# Lancement : du 19 novembre au 6 janvier, jour par jour

Méthode : `founder-launch`. Matière : `board.md` (sa checklist est la colonne vertébrale), `offer.md`, `pricing.md`, `cfo.md`, `panel/results.md` (v2 : 5 achats sur 30), `panel-v1/results.md` (0 sur 20), `idea.md`, `site-notes.md`. Le calendrier marketing des 30 jours est dans `marketing.md`, la checklist légale et le registre des risques dans `ops.md`, la carte de résultat et les textes de notification dans `brand.md` : ce plan les appelle, il ne les réécrit pas.

Aujourd'hui : jeudi 19 novembre 2026. Sortie payante visée : **lundi 7 décembre 2026**. Date de repli : **lundi 14 décembre**. Laurène dispose de 15 h par semaine (soirs de semaine ~1 h 30, mardi 3 h, samedi et dimanche 3 h chacun) ; Jules prend tout ce qui n'est pas du code.

## 1. Le test réel avant de dépenser

### Test A : la pré-vente fondateurs

Le produit est un abonnement : le test le moins cher est l'offre fondateurs payée d'avance. **49 €/an pour le couple, 100 places, jusqu'au 31 décembre, encaissé via un lien de paiement Stripe** (pas de promesse, pas de liste d'attente : une carte bancaire).

**Ligne de succès, écrite avant de lancer : 10 couples payants parmi les 50 couples bêta avant le lundi 7 décembre** (objectif des fondateurs, repris dans `pricing.md`). Le lien de paiement ne peut exister qu'une fois l'entité créée et Stripe activé en mode réel (section 2). S'il n'est pas en ligne le lundi 30 novembre, la ligne est mesurée 7 jours après sa mise en ligne, au plus tard à la revue du 14 décembre.

**Règle de comparaison avec le panel.** Le panel v2 achète à 17 % (5 sur 30) ; 10 sur 50 ferait 20 %. Trois issues :
- **10 ou plus** : les vrais acheteurs confirment le panel ; on lance et les 600 € de janvier restent en jeu (décision finale le 6 janvier, section 4).
- **5 à 9** : on lance, mais les 600 € sont gelés tant que le canal qui a amené ces couples n'a pas un coût connu.
- **Moins de 5** : les vrais acheteurs disent non là où le panel disait oui ; on les croit. Retour à `/founder-offer` (mode solo et « lettre au partenaire », les deux ajouts v3 demandés par le re-test) ou à `/founder-pricing` **avant** le premier euro des 600 € de janvier. Le lancement du 7 décembre reste (il ne coûte rien), la pub non.

À noter aussi *qui* paie : le panel dit que les acheteuses sont les couples qui ont déjà un rituel à deux (4 sur 4) et les jeunes mamans (3 sur 7). Jules note le profil de chaque couple fondateur ; si les 10 viennent de ces deux groupes, `marketing.md` cible là.

### Test B : le blocage n° 1 du panel

22 refus sur 25 tiennent à une phrase : « mon partenaire ne le fera jamais ». Aucune offre ne tranche ça ; seuls de vrais couples le peuvent. Sur les 50 couples bêta, on mesure dès le 30 novembre :
- **le taux d'acceptation de l'invitation partenaire : objectif ≥ 30 %** (KPI des fondateurs). En dessous de 30 %, le mode solo et la lettre au partenaire passent devant toute autre brique de janvier ;
- **le retour à J1 et à J7** après le premier soir à deux. Le board exige un objectif J7 fixé avant le 7 décembre et les fondateurs ne l'ont pas encore écrit : proposition à valider, 50 % des couples qui ont démarré l'essai reviennent au septième soir, la même barre que pour la complétion du test.

Ces deux chiffres, plus les tests complétés et les comptes créés, sont la première condition du board (« chiffres réels d'aujourd'hui ») : Laurène les sort de Clarity et Supabase cette semaine, avant toute autre tâche.

## 2. Le compte à rebours

Légende : **[CC]** = chemin critique, une glissade décale la date de sortie. L = Laurène, J = Jules.

### Semaine 1 : jeudi 19 → dimanche 22 novembre

| quoi | qui | échéance |
|---|---|---|
| **[CC] Déclarer la micro-entreprise** (guichet unique) ; checklist et pièces dans `ops.md` | J | ven. 20 nov. |
| Chiffres réels du site (tests complétés, comptes, invitations, J1/J7) sortis de Clarity et Supabase, 1 h | L | ven. 20 nov. |
| **[CC] Migration de domaine** : redirections app.myrelation.fr → mylovelab.fr préparées (DNS, liens dans les e-mails et sur /duo), soirs jeu. et ven. | L | ven. 20 nov. (préparation) |
| **Brique 1 : Stripe réel et offre fondateurs**, en mode test : produit Duo 9,90 €/mois et 59 €/an, prix fondateurs 49 €/an limité à 100, essai de 14 jours qui ne démarre que quand les deux partenaires ont fait le test, résiliation en un clic depuis le compte (6 h, sam. et dim.) | L | dim. 22 nov. |
| Liste nominative des 50 couples bêta visés : réseaux personnels des deux écoles, couples des 4 praticiens positifs, abonnés Instagram, couples « à rituel » (jeux de cartes, questions du soir) | J | dim. 22 nov. |
| Relance personnelle des 4 praticiens positifs : page partenaire, code ?ref=, Duo offert, « envoyez-nous 2 couples pour la bêta » | J | dim. 22 nov. |

### Semaine 2 : lundi 23 → dimanche 29 novembre

| quoi | qui | échéance |
|---|---|---|
| **[CC] Migration de domaine terminée** : plus aucune URL myrelation dans le tunnel test → compte → invitation → session (soirs lun. et mar., 4 h 30) | L | mar. 24 nov. |
| Marketing J−14 : début du calendrier de `marketing.md` (contenu Instagram, messages bêta, préparation du mail de lancement) | J | lun. 23 nov. |
| **[CC] Suivi SIRET** ; dès réception : ouverture du compte bancaire pro puis activation de Stripe en mode réel (identité, IBAN) ; les délais de l'administration et de la banque ne dépendent pas des fondateurs, d'où le chemin critique | J | dès réception, au plus tard ven. 4 déc. |
| Pages légales en ligne : mentions, CGV, droit de rétractation, garantie 30 jours, rappel avant fin d'essai, selon la liste de `ops.md` (relecture, pas un conseil juridique) ; intégration par L le soir du mer. 25 | J (texte), L (mise en ligne) | jeu. 26 nov. |
| **Brique 2 : mails automatiques** = le mécanisme du lendemain exigé par le board : bienvenue, question du soir par e-mail à 20 h avec la question dedans, rappel 3 jours avant la fin de l'essai, confirmation d'annulation (Brevo) ; plus le check-in du soir (6 h, sam. et dim.) | L | dim. 29 nov. |
| Les **sons** (gamification) sortent de la liste d'avant-lancement : pas sur la boucle, pas le temps. Janvier au plus tôt. | L | décision ce dimanche |
| **Gel du code** : à partir du dimanche 29 novembre 22 h, uniquement des corrections de bugs | L | dim. 29 nov. |
| Recrutement bêta : 25 couples inscrits (compte créé) ; messages personnels, pas de canal froid (ils ont échoué) | J | dim. 29 nov. |
| Créatrices : 10 contactées avec l'argument « 30 % sur 12 mois + un test gratuit que ton audience partage en story » ; objectif réaliste avant le 7 déc. : les premières réponses, pas 10 signatures | J | dim. 29 nov. |

### Semaine 3 : lundi 30 novembre → dimanche 6 décembre

| quoi | qui | échéance |
|---|---|---|
| **Ouverture douce** (friends-and-family) : 10 couples passent les coutures une par une, test → invitation → compte → essai (mode test ou réel) → session à deux → e-mail du soir reçu ; chaque couture est cochée dans `ops.md` par un couple, puis par dix | J (suivi), L (correctifs) | mer. 2 déc. |
| Carte de résultat « Vos deux regards » et textes de notification tels que livrés par `brand.md`, intégrés mardi 1er déc. (3 h) ; dans la même soirée, manifest PWA (icône sur l'écran d'accueil) si les correctifs le laissent. **Le web push ne tient pas dans 15 h** : l'e-mail du soir est le rappel de lancement, le push arrive en janvier | L | mar. 1er déc. |
| **[CC] Lien de paiement fondateurs en ligne dès que Stripe est en mode réel** ; envoi aux couples bêta par J le jour même ; départ du test A | L (lien), J (envoi) | dès activation, au plus tard ven. 4 déc. |
| Recrutement bêta : 50 couples inscrits | J | dim. 6 déc. |
| Praticiens : les 4 positifs actifs (page, code, au moins un couple envoyé). Les 156 autres sont relancés avec le test gratuit « pour vos couples en salle d'attente » ; l'objectif de 20 praticiens actifs passe au 31 janvier, à 2,5 % de réponse il n'est pas atteignable en 18 jours | J | ven. 4 déc. |
| **GO / NO-GO, vendredi 4 décembre, 19 h** (critères ci-dessous) | L + J | ven. 4 déc. |
| Répétition du déroulé du 7 décembre (section 3), déploiement final dimanche 18 h, page /duo mise à jour (« bêta gratuite » remplacée par l'essai de 14 jours et l'offre fondateurs) | L | dim. 6 déc. |

**Critères du go, vendredi 4 décembre.** Tous les critères durs, sinon no-go.
1. *Dur* : micro-entreprise créée (SIRET reçu), compte bancaire ouvert, Stripe activé en mode réel.
2. *Dur* : migration de domaine terminée.
3. *Dur* : les coutures invitation, paiement, session partagée et e-mail du soir passées par 10 couples de l'ouverture douce sans correctif ouvert.
4. *Dur* : l'e-mail du soir est parti automatiquement à 20 h trois soirs de suite (2, 3 et 4 décembre).
5. *Dur* : pages légales en ligne (liste `ops.md`).
6. *Souple* : 30 couples bêta inscrits. En dessous, on lance quand même, mais les 150 € de Noël restent gelés jusqu'à 30 inscrits.

**Règle du repli.** Pas d'entité au 4 décembre : la sortie glisse au **lundi 14 décembre**, avec un second go/no-go le **vendredi 11 décembre**. On ne lance pas sans entité, même « pour quelques jours », même en mode test : c'est la condition du board et la loi. Après le 14 décembre, pas de lancement la semaine de Noël : la date suivante est le lundi 4 janvier 2027 et l'offre fondateurs est re-datée.

### Du 7 au 31 décembre (hors run sheet)

| quoi | qui | échéance |
|---|---|---|
| Revue J7 | L + J | lun. 14 déc. |
| 150 € de la vague de Noël : débloqués seulement après le go et après 10 couples passés par les coutures (condition du board : aucun euro de pub avant) ; canal et dates dans `marketing.md` ; chaque euro étiqueté par canal pour obtenir un coût par couple | J | pas avant le 14 déc. |
| Revue J14 | L + J | lun. 21 déc. |
| Fin de l'offre fondateurs à minuit ; passage à 59 €/an ; compte des places vendues | L | jeu. 31 déc. |
| Corrections de bugs uniquement ; aucune brique nouvelle (section 5) | L | tout décembre |

## 3. Le jour J : lundi 7 décembre 2026

Hypothèse de disponibilité : Laurène libre avant 8 h, de 12 h à 13 h et après 19 h ; Jules joignable toute la journée. Tout ce qui demande du code attend un créneau de Laurène ; entre deux, Jules applique les parades du registre des risques de `ops.md`.

| heure | qui | quoi |
|---|---|---|
| 6 h 45 – 7 h 45 | L | Bascule : page tarifs et offre fondateurs visibles, bandeau « bêta gratuite » retiré. Achat réel de contrôle à 49 € depuis un compte test, vérification du webhook Stripe (essai créé dans Supabase, e-mail de bienvenue reçu), puis remboursement. Un lien d'invitation généré et ouvert sur un second téléphone. |
| 7 h 45 | L → J | Message « c'est ouvert » avec l'état des trois contrôles. Si l'un échoue, voir « si ça casse ». |
| 8 h 00 | J | Mail de lancement aux couples bêta et à la liste : l'offre fondateurs, le lien de paiement, le test gratuit à envoyer au partenaire. Texte dans `marketing.md`. |
| 8 h 30 | J | Instagram : post + story (carte « Vos deux regards » de `brand.md`), lien en bio vers le test. |
| 9 h – 12 h | J | Messages personnels un par un aux 50 couples bêta et aux 4 praticiens (leur lien ?ref=). Surveillance du tableau Stripe et des DM. Jules ne touche pas au code. |
| 12 h – 13 h | L | Point technique : événements Stripe, invitations créées vs acceptées, taux d'ouverture du mail de 8 h. Correctifs urgents seulement. |
| 13 h – 19 h | J | Réponses aux questions, relance des praticiens, premiers contacts créatrices avec le lien du jour ; note de tout ce qui bloque un couple. |
| 19 h – 20 h | L | Contrôle avant la première question du soir : contenu, lien, heure d'envoi. |
| 20 h 00 | auto | **Première question du soir par e-mail** à tous les couples en essai. |
| 20 h – 21 h 30 | L + J | Taux d'ouverture et de réponse à la question ; liste des bugs ; chiffres du jour (tests, invitations, essais, paiements) dans le tableau de la section 4. Debrief 15 min, priorité unique pour mardi. |

**L'offre du jour** : l'offre fondateurs, 49 €/an pour deux, 100 places jusqu'au 31 décembre, satisfait ou remboursé 30 jours, résiliable en un clic. Pas d'autre remise, pas de compte à rebours artificiel.

**Si ça casse** (parades à détailler dans `ops.md`) :
- *Webhook Stripe muet* (paiement reçu, essai non activé) : Jules répond au couple dans l'heure, Laurène active l'essai à la main dans Supabase à 12 h ou à 19 h ; si plus de deux cas avant midi, Jules retire le lien de paiement du mail et des stories, le test gratuit continue de tourner.
- *Lien d'invitation cassé* : Jules envoie au partenaire le code à 6 caractères de la page /duo, valable 7 jours ; Laurène corrige au prochain créneau.
- *E-mail du soir non parti à 20 h* : Jules envoie la question à la main aux couples en essai avant 21 h ; mardi, Laurène repasse la tâche planifiée. Le push n'existe pas encore, il n'y a donc pas de canal à perdre.
- *Site ou domaine en panne* : retour au dernier déploiement du dimanche 6 ; aucune annonce avant que l'achat de contrôle repasse.

## 4. Les 30 premiers jours

### Les chiffres de la semaine (tableau tenu par Jules, tous les lundis)

| chiffre | source | niveau qui déclenche un changement |
|---|---|---|
| Tests terminés / commencés | Clarity, Supabase | < 50 % : on retravaille le test, pas le reste |
| Invitations acceptées / envoyées | Supabase | < 30 % : mode solo et lettre au partenaire passent en tête de janvier |
| Essais démarrés (les deux ont fait le test) | Stripe | aucun essai sur une semaine : la couture invitation → essai est cassée |
| Essais qui atteignent le 7e soir | Supabase | < objectif J7 fixé (proposition 50 %) : le rappel du lendemain est le chantier de janvier, push en premier |
| Couples payants (cumul) vs seuil de 36 | Stripe | la trajectoire : 10 fondateurs au 31 déc. ; le seuil de 36 (`cfo.md`) est l'horizon, pas la barre du mois |
| Paiements / tests terminés | Stripe ÷ Supabase | < 3 % : retour à l'offre avant la pub |
| Remboursements / paiements | Stripe | > 15 % (haut de la fourchette modélisée dans `offer.md`) : chercher le motif, suspendre la pub |
| Coût par couple payant, par canal | dépenses étiquetées ÷ couples payants de ce canal | > 30 € (valeur d'un couple, `cfo.md`) : on coupe le canal ; viser 10 € |

### Les trois revues

**J7, lundi 14 décembre.** Le test A est-il concluant (10 couples payants, ou combien) et dans quel groupe sont-ils ? Le taux d'invitation est-il au-dessus de 30 % ? Combien de couples sont revenus le lendemain de leur premier soir ? Les 150 € de Noël partent-ils, et sur quel canal ? Qu'est-ce qui a cassé le jour J et qu'est-ce qui a été corrigé ? Si no-go le 4 décembre, cette date devient le jour J et la revue glisse au 21.

**J14, lundi 21 décembre.** Les premiers essais de 14 jours arrivent à échéance : combien convertissent, combien annulent, et que disent ceux qui annulent ? Le rappel J−3 avant fin d'essai est-il parti ? Y a-t-il un canal dont le coût par couple est connu et inférieur à 30 € ? Les 4 praticiens ont-ils envoyé au moins un couple chacun ? Les 50 couples bêta sont-ils tous passés par le test ?

**J30, mercredi 6 janvier 2027. La décision sur les 600 € de janvier.** On dépense si, et seulement si : (1) au moins 10 couples payants fondateurs au 31 décembre ; (2) invitation ≥ 30 % et J7 au-dessus de l'objectif fixé ; (3) remboursements ≤ 15 % ; (4) un canal mesuré sur les 150 € de Noël avec un coût par couple ≤ 30 €, car les 600 € doivent produire au moins 20 couples payants pour ne pas être perdus (`cfo.md`). Sinon on garde l'argent, on retourne à `/founder-offer` ou `/founder-pricing`, et la Saint-Valentin (1 000 €) se décide à la revue du 6 février sur les mêmes critères. Également le 6 janvier : la boucle a-t-elle été mesurée sur 50 couples ? Si oui, le gel de la section 5 peut être rediscuté ; sinon il tient.

## 5. Ce qui est gelé

Jusqu'à ce que la boucle **test → Duo → retour le lendemain** ait été mesurée sur 50 couples (invitation, essai, J1, J7, paiement), conformément au board, rien de ceci n'est codé ni annoncé :
- le jeu de cartes-questions,
- le calendrier des dates (au-delà de ce qui existe sur /duo),
- les podcasts,
- la version anglaise,
- la carte cadeau Duo (elle revient pour la Saint-Valentin seulement si le gel est levé le 6 janvier),
- les sons et la gamification au-delà des streaks existants,
- le pack « une dimension » à 14,90 € (`pricing.md` : plus tard).

Les seules briques autorisées en janvier sont celles que les chiffres de la section 4 réclament : le web push PWA si J7 est sous l'objectif, le mode solo et la lettre au partenaire si l'invitation est sous 30 %. Une seule à la fois, dans les 15 h de Laurène.

Prochaine étape : `/founder-plan` compile le tout dans le plan d'affaires.
