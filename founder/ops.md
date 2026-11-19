# Opérations : comment MyLoveLab tourne à partir du 7 décembre

Adapté de la méthode `founder-ops` à un abonnement en ligne : pas de fournisseurs de marchandises, pas de local. Sources : `idea.md`, `offer.md`, `pricing.md`, `numbers.json`, `cfo.md`, `site-notes.md`, `/tracking/`. Prix publics relevés le 19/11/2026 (à revérifier au moment de payer) ; les estimations sont marquées. **Rien ici n'est un conseil juridique, comptable ou fiscal** : chaque point de la section 6 est à confirmer avec l'administration ou un professionnel.

## 1. Le cycle quotidien et hebdomadaire une fois en ligne

Ce que voit le couple est marqué **[client]**.

**Automatique, sans intervention**
- **[client]** Test gratuit sans compte → création de compte → code d'invitation à 6 caractères → le partenaire fait le test de son côté → « Vos deux regards » s'affiche quand les deux ont fini → l'essai Stripe de 14 jours démarre à cet instant (brique 1).
- **[client]** 20 h 30 : notification web push avec la question du soir (PWA, brique 2) ; si le push n'est pas accepté ou pas délivré sous 10 min, e-mail de secours (brique 3). J-3 avant la fin de l'essai : e-mail « votre essai se termine, 9,90 €/mois ou 59 €/an, résiliez en un clic ».
- Stripe : encaissement, relances d'échec de paiement (Smart Retries), facture par e-mail, reçu de remboursement, suspension de l'accès si impayé via webhook `customer.subscription.updated`.
- Supabase : sauvegardes quotidiennes (plan Pro), journal des webhooks reçus dans une table `stripe_events`.
- Clarity et GA4 (version avec consentement de `head-tracking.html`) : enregistrement des parcours et des événements `test_termine`, `invitation_envoyee`, `invitation_acceptee`, `essai_demarre`, `paiement`.

**Chaque jour, 15 min (Laurène le matin, Jules en secours)** : routine 1 ci-dessous ; réponse aux messages de `contact@mylovelab.fr` **[client]** sous 24 h en semaine, 48 h le week-end.

**Chaque semaine**
- Lundi soir (Jules, 45 min) : tableau de bord de la semaine (tests terminés, invitations acceptées, essais démarrés, paiements, churn, remboursements) comparé aux KPI tunnel (≥ 50 % de tests terminés, ≥ 30 % d'invitations, ≥ 3 % de paiement).
- Mardi (Laurène, 3 h) : corrections produit issues des tickets de la semaine ; déploiement Vercel en préversion puis production.
- Vendredi (Jules, 1 h) : relevé des commissions d'affiliation, paiement le 5 du mois suivant (routine 5), message aux affiliées **[affiliée]**.
- Week-end (Laurène, 6 h) : une vague de contenu/SEO (routine 6) et les briques produit encore ouvertes.
- Dimanche soir (les deux, 30 min) : revue des risques (section 7) et de la semaine à venir.

## 2. « Fournisseurs » : les outils et services

| service | rôle | prix public (19/11/2026) | source |
|---|---|---|---|
| Vercel Pro | hébergement, usage commercial (Hobby interdit) | 20 $/mois par membre ≈ 18,50 € | [vercel.com/pricing](https://vercel.com/pricing) |
| Supabase Pro | base, auth, sauvegardes 7 jours, pas de mise en pause | 25 $/mois ≈ 23 € (10 $ de calcul inclus) | [supabase.com/pricing](https://supabase.com/pricing) |
| Stripe | abonnements, essai, remboursements, codes promo | 1,5 % + 0,25 € par carte UE ; 2,5 % + 0,25 € carte UK ; 3,25 % hors UE | [stripe.com/fr/pricing](https://stripe.com/fr/pricing) |
| Brevo (e-mails) | rappels et transactionnels | gratuit jusqu'à 300 e-mails/jour ; Starter dès ≈ 7 € HT/mois (5 000 e-mails) | [brevo.com/fr/pricing](https://www.brevo.com/fr/pricing/) |
| Resend (alternative dev) | e-mails via API | gratuit 3 000/mois (100/jour) ; Pro 20 $/mois (50 000) | [resend.com/pricing](https://resend.com/pricing) |
| Web push | question du soir | gratuit via service worker + VAPID (aucun tiers) ; ou OneSignal gratuit (web push plafonné à 10 000 abonnés par envoi, Growth dès 19 $/mois) | [onesignal.com/pricing](https://onesignal.com/pricing) |
| Microsoft Clarity | enregistrements, cartes de chaleur | gratuit | [clarity.microsoft.com](https://clarity.microsoft.com) |
| GA4 | mesure d'audience | gratuit | [analytics.google.com](https://analytics.google.com) |
| Canva | visuels Instagram | gratuit ; Pro ≈ 110–120 €/an (sources tierces, à vérifier) | [canva.com/fr_fr/tarifs](https://www.canva.com/fr_fr/tarifs/) |
| Registrar (OVHcloud) | mylovelab.fr + myrelation.fr | .fr ≈ 7,79 € HT/an au renouvellement, soit ≈ 19 € TTC/an pour deux | [ovhcloud.com/fr/domains](https://www.ovhcloud.com/fr/domains/tld/fr/) |
| Banque (Shine) | compte dédié, obligatoire au-delà de 10 000 € de CA deux ans de suite | offre gratuite ; Start ≈ 9 € HT/mois | [shine.fr/tarifs](https://shine.fr/tarifs) |
| Affiliation | suivi des commissions | **option A** : codes promo Stripe + cookie `?ref=` stocké dans Supabase, 0 € ; **option B** : Rewardful dès 49 $/mois, Tolt dès 69 $/mois | [rewardful.com/pricing](https://www.rewardful.com/pricing), [tolt.io/pricing](https://tolt.io/pricing) |

**Ce qui diffère de `numbers.json` (le CFO doit relancer, je n'ai pas modifié le fichier)**
1. **Cotisations micro : 25,6 % en 2026 pour le BNC**, pas 24,6 % (taux 2025). Si l'activité est classée « prestation de services commerciale » (BIC), c'est 21,2 %. L'**ACRE** passe de 50 % à 25 % d'exonération au 1er juillet 2026 et n'est plus automatique. Source : [economie.gouv.fr, cotisations micro](https://www.economie.gouv.fr/entreprises/micro-entreprise-auto-entreprise-charges-sociales). Impact : +0,08 €/couple-mois (BNC) ou −0,27 € (BIC). À trancher avec l'URSSAF.
2. **E-mailing : 0 € au lancement** (plan gratuit Brevo, 300/jour suffit jusqu'à ≈ 120 couples à 2 rappels/jour) puis ≈ 7 € HT au lieu de 9 €.
3. **Domaines : ≈ 1,60 €/mois** au lieu de 2 € (écart négligeable).
4. À ajouter en option : RC pro ≈ 13 €/mois (estimation, section 6) ; outil d'affiliation 49 $/mois seulement si l'option A ne tient plus (au-delà de ~30 affiliées).

## 3. Les gens

Deux cofondateurs, personne payé, aucun salarié ; aucune charge de paie, mais le temps n'est pas valorisé (`cfo-sources.md`). Laurène : 15 h/semaine (soirs de semaine ≈ 1 h 30 lundi, mercredi, jeudi, vendredi ; mardi 3 h ; samedi 3 h ; dimanche 3 h). Jules : volume non précisé, **estimation** 10 h/semaine, à confirmer.

| créneau | mois 1 (lancement, 10–25 couples) | à 300 couples |
|---|---|---|
| Laurène, matin 15 min | routine 1 | routine 1 |
| Laurène, lundi/mer/jeu/ven soir 1 h 30 | bugs du jour, support technique (invitations, push), suivi des 50 couples bêta | support de 2e niveau (≈ 1 ticket sur 5), bugs, données RGPD |
| Laurène, mardi 3 h | déploiement des correctifs, A/B prix | idem + analyse rétention J7/J30 |
| Laurène, samedi 3 h | contenu (1 article SEO ou 2 posts) | contenu |
| Laurène, dimanche 3 h | brique produit (mode solo, lettre au partenaire) | produit |
| Jules, chaque jour 20 min | boîte `contact@`, 1er niveau | boîte `contact@`, 1er niveau (≈ 2–4 tickets/jour, estimation 1 %/jour des couples) |
| Jules, lundi 45 min | tableau de bord | tableau de bord + rapport affiliées |
| Jules, semaine | praticiens et créatrices (objectif 20 + 10), Instagram 2 posts | affiliées, partenariats, pub (Meta/TikTok) |
| Jules, vendredi 1 h | commissions | commissions, réponses aux avis |

**SLA support** (affiché sur la page contact) : accusé de réception automatique immédiat ; réponse humaine sous 24 h ouvrées, 48 h le week-end ; remboursement lancé sous 48 h ; message évoquant un danger : le jour même (routine 4). À 300 couples, si les tickets dépassent 5/jour pendant deux semaines, ouvrir une FAQ et des réponses types avant de penser à de l'aide payée.

## 4. Les routines (SOP)

**Routine 1 : contrôle du matin (15 min)**
1. Stripe → Accueil : paiements de la nuit, échecs, litiges (un litige = réponse sous 7 jours avec l'historique d'usage). Webhooks → aucun événement en échec ; sinon routine 7.
2. Supabase → Reports : erreurs API, taille de la base ; vérifier que la sauvegarde de la nuit existe.
3. Vercel → Deployments : dernier déploiement vert ; Logs : erreurs 5xx.
4. Clarity : session rage-click ou erreur JS sur `/test`, `/duo`, paiement.
5. `contact@` : trier en 4 étiquettes (technique, remboursement, danger, autre) ; répondre à « danger » tout de suite.
6. Noter dans le tableau de bord : tests terminés, invitations acceptées, essais démarrés, paiements, remboursements.

**Routine 2 : demande de remboursement ou de résiliation**
1. **Résiliation** : elle se fait en un clic dans le compte ; si la demande arrive par e-mail, la faire dans Stripe (annuler à la fin de la période) et confirmer par écrit le jour même.
2. **Garantie 30 jours** : si le premier paiement date de moins de 30 jours, rembourser en entier dans Stripe, sans question, sous 48 h ; le remboursement apparaît sur la carte sous 5 à 10 jours ; l'écrire au client.
3. **Rétractation légale** : la vente à distance ouvre 14 jours de rétractation ; pour un contenu numérique à accès immédiat, le droit tombe seulement si le client a consenti expressément au démarrage immédiat et renoncé à la rétractation lors de l'achat (Code de la consommation, art. L221-18 et L221-28, [service-public.fr F10485](https://www.service-public.fr/particuliers/vosdroits/F10485)). Notre garantie 30 jours couvre ce cas ; **pas un conseil juridique**, à faire relire.
4. Après 30 jours : pas de remboursement du mois en cours, résiliation à la fin de la période ; proposer de passer à l'annuel si le motif est le prix.
5. Noter le motif en un mot dans la table `churn` ; au-dessus de 15 % de remboursements, alerter le CFO (`offer.md` modélise 5 %).

**Routine 3 : l'invitation du partenaire échoue**
1. Identifier le cas : code expiré (7 jours), code mal saisi, partenaire qui a créé un compte séparé, e-mail d'invitation en spam.
2. Régénérer un code depuis l'admin Supabase, l'envoyer au client avec un texte prêt à transférer à son partenaire (« fais le test de ton côté, 15 min, pour comparer »).
3. Si deux comptes existent, fusionner côté base (script `link_partners`), ne jamais supprimer les réponses.
4. Rappeler que l'essai ne démarre que quand les deux ont fini : rien n'est facturé en attendant.
5. Compter l'incident ; au-delà de 10 % des invitations, c'est un bug produit, pas du support : mardi suivant.

**Routine 4 : un message qui suggère un danger ou des violences**
1. Répondre le jour même, sur un ton calme, sans diagnostic ni jugement, en une personne (Laurène ou Jules, jamais une réponse automatique seule).
2. Donner les ressources officielles : **3919** (Violences Femmes Info, gratuit, anonyme, 24 h/24, [arretonslesviolences.gouv.fr](https://arretonslesviolences.gouv.fr)) ; en danger immédiat **17** ou **112**, SMS **114** si parler est impossible ; orienter vers un praticien (liste des praticiens partenaires) ou un médecin.
3. Dire clairement que MyLoveLab n'est pas un service d'urgence ni une thérapie ; proposer de suspendre le programme et de délier les comptes si la personne le souhaite.
4. Ne jamais contacter le partenaire, ne jamais révéler qu'un message a été reçu.
5. Consigner la date et la nature du message dans un registre à accès restreint (pas le CRM), sans détails inutiles ; en discuter à deux le dimanche.

**Routine 5 : commissions d'affiliation (vendredi, 1 h ; paiement le 5 du mois)**
1. Export Stripe des abonnements actifs avec code promo ou champ `ref` (table `referrals`).
2. Calcul : 30 % du montant encaissé HT de frais Stripe, pendant 12 mois, sur les paiements non remboursés ; retirer les remboursements du mois.
3. Envoyer à chaque affiliée son relevé ; elle **facture** la commission (micro-entrepreneuse avec SIRET, pas de salaire) ; payer par virement dans les 30 jours de la facture.
4. Rapport : couples apportés, taux de conversion par affiliée, coût d'acquisition (plafond 30 €, cible 10 €, `cfo.md`).

**Routine 6 : vague contenu/SEO (week-end, 3 h)**
1. Un article de blog ciblé sur une requête du tunnel (« on se dispute tout le temps », « style d'attachement ») ou une page par paire de profils ; sources citées, règle éditoriale : « session ludique », pas d'étiquette figée, jamais « sauver son couple ».
2. Deux posts Instagram (Canva) ; mention « collaboration commerciale » sur tout contenu d'affiliée.
3. Vérifier Search Console : erreurs d'indexation, redirections 301 de myrelation.fr.

**Routine 7 : incident (site down, webhook Stripe en échec)**
1. Vérifier [vercel-status.com](https://www.vercel-status.com), [status.supabase.com](https://status.supabase.com), [status.stripe.com](https://status.stripe.com).
2. Site down : revenir au déploiement précédent dans Vercel (« Promote to production ») ; message sur Instagram si > 1 h.
3. Webhook en échec : Stripe réessaie automatiquement pendant environ 3 jours (chiffre de sources tierces, à vérifier dans [docs.stripe.com](https://docs.stripe.com/webhooks)) puis désactive l'endpoint ; corriger, puis renvoyer les événements depuis Développeurs → Webhooks (possible 15 jours) ; l'endpoint doit ignorer les doublons (`stripe_events`).
4. Base inaccessible : ne rien écrire à la main ; attendre la restauration ; si perte de données, restaurer la sauvegarde de la veille (Pro) et prévenir les couples concernés.
5. Écrire 5 lignes de post-mortem le dimanche.

**Routine 8 : checklist d'avant-lancement (à cocher le 6 décembre)**
- [ ] Entité créée, SIRET reçu, compte Stripe activé (KYC) et premier virement test reçu.
- [ ] Prix Duo 9,90 €/mois et 59 €/an, offre fondateurs 49 €/an (100 places, 31/12) ; essai conditionnel testé par les fondateurs puis par 10 couples bêta.
- [ ] PWA installable (iOS et Android), push reçu à 20 h 30, e-mail de secours reçu ; e-mail J-3 avant fin d'essai.
- [ ] Résiliation en un clic ; garantie 30 jours sur la page de paiement ; consentement exprès à l'accès immédiat et renonciation à la rétractation.
- [ ] CGV/CGU, mentions légales, politique de confidentialité, bandeau cookies (version consentement de `head-tracking.html`), 3919 dans le pied de page.
- [ ] Migration myrelation.fr → mylovelab.fr : 301 page par page, sitemap, Search Console, GA4 et Clarity sur le nouveau domaine.
- [ ] Sauvegarde manuelle de Supabase le 6 décembre ; clé Stripe live hors du dépôt ; webhook live signé.
- [ ] Page contact avec SLA ; réponses types prêtes (routines 2, 3, 4).

## 5. La pile minimale et son coût

Vercel Pro 18,50 € + Supabase Pro 23 € + Stripe (variable) + Brevo gratuit puis ≈ 7 € + web push maison 0 € + Clarity et GA4 0 € + Canva gratuit + domaines ≈ 1,60 € + Shine gratuit (ou 9 €) + IA 90 € (estimation, 20 € si Claude Pro suffit) ≈ **133 à 160 €/mois**, cohérent avec les 152 € de `numbers.json`. Affiliation par codes promo et cookie `?ref=` : 0 € jusqu'à ≈ 30 affiliées. Comptabilité : tableur + déclaration URSSAF mensuelle en micro ; comptable (≈ 50 €/mois, estimation) seulement en société.

## 6. Checklist légale et administrative (France)

Chaque ligne : **à confirmer avec l'autorité ou un professionnel**. Pas un conseil juridique.

1. **Structure.** Une micro-entreprise est individuelle : **un seul titulaire**, impossible à deux ([bpifrance-creation.fr](https://bpifrance-creation.fr/encyclopedie/structures-juridiques/statuts-particuliers/intermediaires-du-commerce-agent-commercial)). Micro au nom de Laurène : gratuite, créée en quelques jours sur le [guichet unique](https://formalites.entreprises.gouv.fr), franchise de TVA, cotisations ≈ 25,6 % (ou 21,2 %) du CA ; **mais** le revenu ne peut pas être partagé avec Jules et deux personnes qui agissent en associés risquent la requalification en société de fait. SAS à deux : ≈ 230–300 € (annonce légale + greffe, estimation), statuts + pacte d'associés, comptable ≈ 50 €/mois, IS, mais répartition 50/50 et propriété de la marque et du code par la société. **Recommandation** : micro Laurène tout de suite pour tenir le 7 décembre, avec un accord écrit signé entre les deux (répartition 50/50 du futur, propriété intellectuelle, engagement de créer une SAS dès que le CA dépasse ≈ 2 000 €/mois ou qu'un euro doit être partagé) ; à valider avec un expert-comptable, car cet accord ne remplace pas une société.
2. **SIRET avant Stripe.** Stripe vérifie l'identité, l'adresse et l'entité (KYC) : liste des pièces acceptées pour la France sur [docs.stripe.com](https://docs.stripe.com/acceptable-verification-documents?country=FR). Sans SIRET, pas de virement vers le compte bancaire. Compter 1 à 3 semaines entre la demande au guichet unique et le premier virement (estimation).
3. **CGV/CGU et mentions légales** : identité de l'éditeur, hébergeur, médiateur de la consommation, prix TTC, durée, résiliation, garantie ([economie.gouv.fr, DGCCRF](https://www.economie.gouv.fr/dgccrf)).
4. **RGPD.** Les réponses au test portent sur la vie affective et sexuelle du couple : **données de l'article 9** (vie sexuelle, santé-adjacent), donc traitement interdit sauf consentement explicite, enregistré, pour chaque personne ; chiffrement, hébergement UE (Supabase Francfort ou Paris), **registre des traitements obligatoire** (l'exemption « moins de 250 salariés » tombe en présence de données sensibles), analyse d'impact (AIPD) probable, DPO non obligatoire. [cnil.fr, registre](https://www.cnil.fr/fr/le-registre-des-activites-de-traitement). Délier les comptes = chaque partenaire garde ses propres réponses ; suppression sur demande sous 30 jours.
5. **Cookies.** GA4 et Clarity n'entrent pas dans l'exemption CNIL de mesure d'audience : consentement préalable, bandeau avec refus aussi facile que l'acceptation, **version avec consentement** de `head-tracking.html`, pixels Meta/TikTok derrière le même bandeau ([cnil.fr, mesure d'audience](https://www.cnil.fr/fr/mesurer-la-frequentation-de-vos-sites-web-et-de-vos-applications)).
6. **TVA.** Franchise en base : 37 500 € de CA pour les services (le seuil unique à 25 000 € voté en 2025 a été suspendu puis non repris dans la loi de finances 2026, [service-public.fr F21746](https://entreprendre.service-public.fr/vosdroits/F21746)). Au-delà, ou en SAS, 20 % de TVA : 9,90 € TTC = 8,25 € HT.
7. **Rétractation** : 14 jours ; renonciation expresse à l'accès immédiat (routine 2) ; rappel avant reconduction.
8. **Loi influenceurs** (loi n° 2023-451 du 9 juin 2023) : mention « publicité » ou « collaboration commerciale » lisible pendant toute la durée du contenu ; contrat écrit avec chaque créatrice ([vie-publique.fr](https://www.vie-publique.fr/loi/288793-loi-influenceurs-proposition-de-loi-delaporte-vojetta)).
9. **Contrats d'affiliation** : apporteuses d'affaires indépendantes, commission facturée avec SIRET, aucun lien de subordination, pas de salaire ([service-public.fr, agent commercial](https://entreprendre.service-public.gouv.fr/vosdroits/F37410)).
10. **Marque INPI** : 190 € une classe, 40 € par classe supplémentaire (classes 41 et 44 à envisager : 230 €, soit 40 € de plus que `numbers.json`) ; recherche d'antériorité « MyLoveLab » d'abord ([inpi.fr/tarifs](https://www.inpi.fr/tarifs)).
11. **RC pro** : facultative pour cette activité ; ≈ 13 €/mois chez Hiscox ou Orus (estimation, devis en ligne).
12. **Avertissement violences** : « MyLoveLab ne remplace pas une thérapie. En cas de violences : 3919, en danger : 17 » dans le pied de page et dans le test.
13. **Compte bancaire dédié** : obligatoire si le CA dépasse 10 000 € deux ans de suite ([service-public.fr](https://entreprendre.service-public.fr/vosdroits/F32797)).

## 7. Registre des risques

| # | risque | probabilité | impact | plan |
|---|---|---|---|---|
| 1 | **Stripe bloque le compte** (KYC incomplet, activité jugée sensible) | moyenne | élevé : zéro encaissement | SIRET et pièces complètes avant le 1er décembre ; description d'activité claire (« programme de bien-être relationnel ») ; réserve de 2 mois de frais fixes ; plan B : PayPal ou Lemon Squeezy (frais plus élevés) |
| 2 | **Panne Supabase** | faible | élevé | plan Pro avec sauvegardes ; page d'erreur douce ; routine 7 |
| 3 | **La boucle d'invitation casse** après une mise à jour | moyenne | élevé : aucun essai ne démarre | test de bout en bout avant chaque déploiement ; alerte si 0 invitation acceptée en 24 h |
| 4 | **Fuite de données** (clé exposée, RLS mal configurée) | faible | très élevé : données art. 9, notification CNIL sous 72 h | RLS sur toutes les tables, clés hors dépôt, revue trimestrielle ; procédure de notification écrite |
| 5 | **Une utilisatrice en danger** | moyenne | très élevé | routine 4 ; 3919 visible partout ; jamais de réponse automatique seule |
| 6 | **Mauvais avis Trustpilot** | moyenne | moyen | répondre publiquement sous 48 h, rembourser si éligible ; signaler seulement ce qui viole les règles ([Trustpilot, guidelines](https://legal.trustpilot.com/for-businesses/guidelines-for-businesses)) ; témoignages de couples bêta |
| 7 | **Paired copie le test en français** | moyenne à 12 mois | élevé | avance sur le contenu SEO FR, praticiens partenaires, marque déposée ; mesurer le résultat à J7 pour le rendre racontable |
| 8 | **Partiels de Laurène** (janvier, mai) | certaine | moyen : 15 h tombent à 5 h | gel produit annoncé ; Jules tient le support et la routine 1 ; aucune sortie la semaine des examens |
| 9 | **Entité pas prête le 7 décembre** | moyenne | élevé | demande au guichet unique cette semaine ; si SIRET absent le 1er décembre, lancer la pré-vente en « liste d'attente » sans encaisser et décaler le paiement, pas le lancement |
| 10 | **La migration de domaine casse le SEO** | moyenne | moyen : 178 URL, 17 articles | 301 une à une, sitemap, Search Console « changement d'adresse », vérification hebdomadaire 8 semaines |

**Non vérifié faute d'accès direct aux sites** : le délai exact de nouvelle tentative des webhooks Stripe, le tarif Canva Pro en euros, le prix Shine actuel, la position de la CNIL spécifique à Clarity (traité ici comme non exempté, par prudence). Suite : `/founder-launch`.
