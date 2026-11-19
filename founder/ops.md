# Opérations : comment MyLoveLab tourne à partir du 7 décembre

Méthode `founder-ops` adaptée à un abonnement en ligne : pas de marchandises, pas de local. Sources : `idea.md`, `offer.md`, `pricing.md`, `numbers.json`, `cfo.md`, `site-notes.md`, `/tracking/`. Prix publics relevés le 19/11/2026, à revérifier au moment de payer ; estimations marquées. **Pas un conseil juridique, comptable ou fiscal.**

## 1. Le cycle quotidien et hebdomadaire

Ce que voit le couple est marqué **[client]**.

**Automatique**
- **[client]** Test gratuit sans compte → compte → code d'invitation → le partenaire fait le test de son côté → « Vos deux regards » → l'essai Stripe de 14 jours démarre à cet instant (brique 1).
- **[client]** 20 h 30 : web push avec la question du soir (PWA, brique 2) ; sans push délivré sous 10 min, e-mail de secours (brique 3). J-3 avant la fin de l'essai : e-mail « 9,90 €/mois ou 59 €/an, résiliable en un clic ».
- Stripe : encaissement, relances d'impayé, factures, coupure de l'accès par webhook. Supabase : sauvegarde quotidienne, table `stripe_events`. Clarity et GA4 (version consentement de `head-tracking.html`) : événements `test_termine`, `invitation_acceptee`, `essai_demarre`, `paiement`.

**Chaque jour** : routine 1 (15 min, Laurène ; Jules en secours) ; **[client]** réponse à `contact@mylovelab.fr` sous 24 h, 48 h le week-end.

**Chaque semaine** : lundi, tableau de bord (Jules : tests terminés, invitations, essais, paiements, churn, remboursements, face aux KPI ≥ 50 % / ≥ 30 % / ≥ 3 %) ; mardi, correctifs et déploiement (Laurène) ; vendredi, commissions (routine 5) ; week-end, contenu/SEO (routine 6) ; dimanche soir, 30 min à deux sur les risques.

## 2. « Fournisseurs » : outils et services

| service | rôle | prix public | source |
|---|---|---|---|
| Vercel Pro | hébergement commercial (Hobby interdit) | 20 $/mois par membre ≈ 18,50 € | [vercel.com/pricing](https://vercel.com/pricing) |
| Supabase Pro | base, auth, sauvegardes 7 j, pas de pause | 25 $/mois ≈ 23 € | [supabase.com/pricing](https://supabase.com/pricing) |
| Stripe | abonnements, essai, remboursements, codes promo | 1,5 % + 0,25 € carte UE ; 2,5 % UK ; 3,25 % hors UE | [stripe.com/fr/pricing](https://stripe.com/fr/pricing) |
| Brevo (ou Resend) | rappels et transactionnels | gratuit ≤ 300 e-mails/jour, Starter ≈ 7 € HT/mois ; Resend gratuit 3 000/mois, Pro 20 $ | [brevo.com](https://www.brevo.com/fr/pricing/), [resend.com](https://resend.com/pricing) |
| Web push | question du soir | service worker + VAPID : 0 € ; ou OneSignal gratuit (≤ 10 000 abonnés web par envoi), Growth dès 19 $/mois | [onesignal.com/pricing](https://onesignal.com/pricing) |
| Clarity, GA4 | mesure, enregistrements | gratuits | [clarity.microsoft.com](https://clarity.microsoft.com) |
| Canva | visuels | gratuit ; Pro ≈ 110–120 €/an (sources tierces) | [canva.com/fr_fr/tarifs](https://www.canva.com/fr_fr/tarifs/) |
| OVHcloud | mylovelab.fr + myrelation.fr | .fr ≈ 7,79 € HT/an, ≈ 19 € TTC pour deux | [ovhcloud.com](https://www.ovhcloud.com/fr/domains/tld/fr/) |
| Shine | compte dédié | gratuit ; Start ≈ 9 € HT/mois | [shine.fr/tarifs](https://shine.fr/tarifs) |
| Affiliation | suivi des commissions | **A** : codes promo Stripe + cookie `?ref=` en base, 0 € ; **B** : Rewardful dès 49 $/mois, Tolt dès 69 $/mois | [rewardful.com](https://www.rewardful.com/pricing), [tolt.io](https://tolt.io/pricing) |

**Écarts avec `numbers.json` (le CFO doit relancer ; fichier non modifié)**
1. **Cotisations micro : 25,6 % en 2026 pour le BNC**, pas 24,6 % (taux 2025) ; 21,2 % si l'activité est classée BIC. L'**ACRE** tombe de 50 % à 25 % d'exonération au 1er juillet 2026 et n'est plus automatique ([economie.gouv.fr](https://www.economie.gouv.fr/entreprises/micro-entreprise-auto-entreprise-charges-sociales)). Impact : +0,08 €/couple-mois (BNC) ou −0,27 € (BIC) ; à trancher avec l'URSSAF.
2. **E-mailing : 0 € au lancement** (300/jour couvrent ≈ 120 couples), puis ≈ 7 € HT au lieu de 9 € ; domaines ≈ 1,60 €/mois au lieu de 2 € ; INPI 230 € si deux classes (41 et 44).
3. Options non chiffrées : RC pro ≈ 13 €/mois ; outil d'affiliation 49 $/mois seulement au-delà de ~30 affiliées.

## 3. Les gens

Deux cofondateurs non payés, aucun salarié, aucune paie. Laurène : 15 h (quatre soirs de 1 h 30, mardi 3 h, samedi 3 h, dimanche 3 h). Jules : **estimation** 10 h/semaine.

| créneau | mois 1 (10–25 couples) | à 300 couples |
|---|---|---|
| Laurène, matin 15 min | routine 1 | routine 1 |
| Laurène, 4 soirs × 1 h 30 | bugs, support technique, suivi des couples bêta | support de 2e niveau (≈ 1 ticket sur 5), bugs, demandes RGPD |
| Laurène, mardi 3 h | correctifs, déploiement, A/B prix | idem + rétention J7/J30 |
| Laurène, samedi et dimanche 3 h + 3 h | contenu (routine 6) ; brique produit (mode solo, lettre au partenaire) | contenu ; produit |
| Jules, 20 min/jour | `contact@`, 1er niveau | `contact@` (≈ 2–4 tickets/jour, estimation 1 % des couples) |
| Jules, lundi 45 min + vendredi 1 h | tableau de bord ; commissions | idem + rapport affiliées |
| Jules, semaine | praticiens et créatrices (20 + 10), Instagram | affiliées, pub Meta/TikTok, avis |

**SLA support**, affiché sur la page contact : accusé de réception immédiat ; réponse humaine sous 24 h ouvrées, 48 h le week-end ; remboursement lancé sous 48 h ; danger : le jour même. Au-delà de 5 tickets/jour deux semaines de suite : FAQ et réponses types avant toute aide payée.

## 4. Les routines (SOP)

**Routine 1 : contrôle du matin (15 min)**
1. Stripe : paiements de la nuit, échecs, litiges (répondre sous 7 jours avec l'historique d'usage) ; webhooks sans échec, sinon routine 7.
2. Supabase : erreurs API, sauvegarde présente. Vercel : déploiement vert, pas de 5xx.
3. Clarity : rage-clicks ou erreurs JS sur `/test`, `/duo`, paiement.
4. `contact@` : trier technique / remboursement / danger / autre ; « danger » d'abord.
5. Noter les chiffres du jour dans le tableau de bord.

**Routine 2 : remboursement ou résiliation**
1. Résiliation : un clic dans le compte ; par e-mail, l'annuler dans Stripe à la fin de la période et confirmer le jour même.
2. Garantie 30 jours : premier paiement de moins de 30 jours → remboursement intégral sous 48 h, sans question ; carte créditée sous 5 à 10 jours.
3. Rétractation légale : 14 jours en vente à distance ; pour un contenu numérique à accès immédiat, le droit tombe seulement si le client a expressément consenti au démarrage et renoncé à la rétractation (Code de la consommation L221-18 et L221-28, [service-public.fr F10485](https://www.service-public.fr/particuliers/vosdroits/F10485)). La garantie couvre ce cas ; à faire relire.
4. Après 30 jours : pas de remboursement du mois en cours ; proposer l'annuel si le motif est le prix. Motif en un mot dans la table `churn` ; au-dessus de 15 % de remboursements, alerter le CFO (modèle à 5 %).

**Routine 3 : l'invitation du partenaire échoue**
1. Cas : code expiré (7 jours), mal saisi, partenaire avec un compte séparé, e-mail en spam.
2. Régénérer un code depuis l'admin, l'envoyer avec un texte à transférer (« fais le test de ton côté, 15 min, pour comparer »).
3. Deux comptes : fusionner côté base, ne jamais effacer de réponses.
4. Rappeler que rien n'est facturé tant que les deux n'ont pas fini ; compter : au-delà de 10 % des invitations, c'est un bug pour le mardi suivant.

**Routine 4 : un message qui suggère un danger ou des violences**
1. Répondre le jour même, calmement, sans diagnostic ni jugement, par une personne, jamais par un automate seul.
2. Donner les ressources officielles : **3919** (gratuit, anonyme, 24 h/24, [arretonslesviolences.gouv.fr](https://arretonslesviolences.gouv.fr)) ; danger immédiat **17** ou **112**, SMS **114** ; orienter vers un praticien partenaire ou un médecin.
3. Dire que MyLoveLab n'est ni un service d'urgence ni une thérapie ; proposer de suspendre le programme et de délier les comptes.
4. Ne jamais contacter le partenaire ni laisser deviner qu'un message a été reçu ; consigner date et nature dans un registre à accès restreint.

**Routine 5 : commissions (vendredi ; paiement le 5 du mois)**
1. Export Stripe des abonnements actifs avec code promo ou `ref` (table `referrals`) ; 30 % de l'encaissé net de frais Stripe, 12 mois, remboursements déduits.
2. Relevé envoyé ; l'affiliée **facture** (micro-entrepreneuse avec SIRET, pas de salaire) ; virement sous 30 jours.
3. Rapport : couples apportés, conversion par affiliée, coût d'acquisition (plafond 30 €, cible 10 €).

**Routine 6 : vague contenu/SEO (week-end, 3 h)**
1. Un article sur une requête du tunnel ou une page par paire de profils ; sources citées ; « session ludique », jamais « sauver son couple ».
2. Deux posts Instagram (« collaboration commerciale » chez les affiliées) ; Search Console : indexation, 301 de myrelation.fr.

**Routine 7 : incident**
1. Vérifier [vercel-status.com](https://www.vercel-status.com), [status.supabase.com](https://status.supabase.com), [status.stripe.com](https://status.stripe.com).
2. Site down : remettre le déploiement précédent en production ; message Instagram si > 1 h.
3. Webhook en échec : Stripe réessaie environ 3 jours (sources tierces, à vérifier sur [docs.stripe.com](https://docs.stripe.com/webhooks)) puis désactive l'endpoint ; corriger, renvoyer les événements depuis le Dashboard ; ignorer les doublons.
4. Base perdue : restaurer la sauvegarde de la veille, prévenir les couples touchés. Post-mortem en cinq lignes le dimanche.

**Routine 8 : checklist d'avant-lancement (6 décembre)**
- [ ] SIRET reçu, Stripe activé (KYC), premier virement test reçu.
- [ ] Duo 9,90 €/mois et 59 €/an, offre fondateurs 49 €/an (100 places, 31/12) ; essai conditionnel testé par les fondateurs puis par 10 couples bêta.
- [ ] PWA installable iOS et Android ; push 20 h 30, e-mail de secours et e-mail J-3 reçus.
- [ ] Résiliation en un clic ; garantie 30 jours sur la page de paiement ; consentement exprès à l'accès immédiat.
- [ ] CGV/CGU, mentions légales, confidentialité, bandeau cookies, 3919 en pied de page.
- [ ] Migration myrelation.fr → mylovelab.fr : 301 page par page, sitemap, Search Console, GA4 et Clarity.
- [ ] Sauvegarde manuelle Supabase ; clés live hors du dépôt ; webhook signé ; réponses types prêtes.

## 5. La pile minimale

Vercel Pro 18,50 € + Supabase Pro 23 € + Brevo 0 puis 7 € + push maison 0 € + Clarity, GA4, Canva 0 € + domaines 1,60 € + Shine 0 (ou 9 €) + IA 90 € (estimation ; 20 € si Claude Pro suffit) = **133 à 160 €/mois**, cohérent avec les 149 € de `numbers.json`. Stripe en variable ; affiliation option A à 0 €. Comptabilité : tableur et déclaration URSSAF mensuelle ; comptable (≈ 50 €/mois) seulement en société.

## 6. Checklist légale et administrative (France)

Chaque ligne : **à confirmer avec l'autorité ou un professionnel**.

1. **Structure.** La micro-entreprise est individuelle : **un seul titulaire**. Micro au nom de Laurène : gratuite, quelques jours via le [guichet unique](https://formalites.entreprises.gouv.fr), franchise de TVA, cotisations 25,6 % (ou 21,2 %) du CA ; **mais** aucun partage de revenu avec Jules, et deux personnes agissant en associés risquent la requalification en société créée de fait. SAS à deux : ≈ 230–300 € (annonce légale + greffe, estimation), statuts et pacte d'associés, comptable ≈ 50 €/mois, IS, 50/50, marque et code détenus par la société. **Recommandation** : micro Laurène maintenant pour tenir le 7 décembre, plus un accord écrit à deux (50/50, propriété intellectuelle, SAS dès ≈ 2 000 €/mois de CA ou dès le premier euro à partager) ; à valider par un expert-comptable.
2. **SIRET avant Stripe.** Stripe vérifie identité, adresse et entité ([pièces acceptées](https://docs.stripe.com/acceptable-verification-documents?country=FR)) ; sans SIRET, pas de virement ; compter 1 à 3 semaines (estimation).
3. **CGV/CGU, mentions légales** : éditeur, hébergeur, médiateur, prix TTC, résiliation, garantie ([DGCCRF](https://www.economie.gouv.fr/dgccrf)).
4. **RGPD.** Les réponses touchent la vie affective et sexuelle : **données de l'article 9**, interdites sauf consentement explicite enregistré pour chaque partenaire ; hébergement UE ; **registre des traitements obligatoire** (l'exemption « moins de 250 salariés » tombe avec des données sensibles) ; AIPD probable ; DPO non obligatoire ([cnil.fr](https://www.cnil.fr/fr/le-registre-des-activites-de-traitement)). Délier : chacun garde ses réponses ; suppression sous 30 jours.
5. **Cookies.** GA4 et Clarity ne relèvent pas de l'exemption CNIL : consentement préalable, refus aussi simple que l'acceptation, version consentement de `head-tracking.html`, pixels Meta/TikTok derrière le même bandeau ([cnil.fr](https://www.cnil.fr/fr/mesurer-la-frequentation-de-vos-sites-web-et-de-vos-applications)).
6. **TVA.** Franchise jusqu'à 37 500 € de CA services ; le seuil unique de 25 000 € voté en 2025 a été suspendu puis écarté de la loi de finances 2026 ([service-public.fr](https://entreprendre.service-public.fr/vosdroits/F21746)). Au-delà ou en SAS : 9,90 € TTC = 8,25 € HT.
7. **Rétractation** : 14 jours, renonciation expresse à l'accès immédiat (routine 2), rappel avant reconduction.
8. **Loi influenceurs** (n° 2023-451 du 9 juin 2023) : « publicité » ou « collaboration commerciale » lisible pendant tout le contenu ; contrat écrit avec chaque créatrice ([vie-publique.fr](https://www.vie-publique.fr/loi/288793-loi-influenceurs-proposition-de-loi-delaporte-vojetta)).
9. **Affiliées** : apporteuses d'affaires indépendantes, commission facturée avec SIRET, aucune subordination, pas de salaire ([service-public.fr](https://entreprendre.service-public.gouv.fr/vosdroits/F37410)).
10. **Marque INPI** : 190 € une classe, 40 € par classe en plus ; antériorité à vérifier d'abord ([inpi.fr/tarifs](https://www.inpi.fr/tarifs)).
11. **RC pro** : facultative, ≈ 13 €/mois (Hiscox, Orus ; estimation).
12. **Avertissement** « Ne remplace pas une thérapie. Violences : 3919. Danger : 17 » en pied de page et dans le test.
13. **Compte dédié** obligatoire au-delà de 10 000 € de CA deux ans de suite ([service-public.fr](https://entreprendre.service-public.fr/vosdroits/F32797)).

## 7. Registre des risques

| # | risque | probabilité | impact | plan |
|---|---|---|---|---|
| 1 | Stripe bloque le compte (KYC, activité jugée sensible) | moyenne | élevé : zéro encaissement | pièces complètes avant le 1er décembre ; activité décrite comme « bien-être relationnel » ; 2 mois de frais en réserve ; plan B PayPal ou Lemon Squeezy |
| 2 | Panne Supabase | faible | élevé | Pro avec sauvegardes ; page d'erreur douce ; routine 7 |
| 3 | La boucle d'invitation casse après un déploiement | moyenne | élevé : aucun essai ne démarre | test de bout en bout avant chaque déploiement ; alerte si 0 invitation en 24 h |
| 4 | Fuite de données (clé exposée, RLS absente) | faible | très élevé : art. 9, notification CNIL sous 72 h | RLS partout, clés hors dépôt, revue trimestrielle |
| 5 | Une utilisatrice en danger | moyenne | très élevé | routine 4 ; 3919 visible ; jamais d'automate seul |
| 6 | Mauvais avis Trustpilot | moyenne | moyen | réponse publique sous 48 h, remboursement si éligible ; signaler seulement ce qui viole les [règles](https://legal.trustpilot.com/for-businesses/guidelines-for-businesses) |
| 7 | Paired copie le test en français | moyenne à 12 mois | élevé | avance SEO FR, praticiens partenaires, marque ; résultat J7 mesuré et racontable |
| 8 | Partiels de Laurène (janvier, mai) | certaine | moyen : 15 h → 5 h | gel produit ; Jules tient routine 1 et le support ; aucune sortie ces semaines-là |
| 9 | Entité pas prête le 7 décembre | moyenne | élevé | guichet unique cette semaine ; sans SIRET le 1er décembre, liste d'attente sans encaisser : décaler le paiement, pas le lancement |
| 10 | La migration de domaine casse le SEO | moyenne | moyen : 178 URL | 301 une à une, « changement d'adresse » dans Search Console, suivi 8 semaines |

**Non vérifié faute d'accès direct aux sites** : délai exact des relances de webhooks Stripe, tarif Canva Pro en euros, grille Shine, position de la CNIL propre à Clarity (traité comme non exempté, par prudence). Suite : `/founder-launch`.
