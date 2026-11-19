# Lancement : du 19 novembre au 6 janvier, jour par jour

Méthode : `founder-launch`. Colonne vertébrale : la checklist de `board.md`. Sources : `offer.md`, `pricing.md`, `cfo.md`, `panel/results.md` (v2 : 5 achats sur 30), `panel-v1/results.md` (0 sur 20). Le calendrier marketing vit dans `marketing.md`, la checklist légale et le registre des risques dans `ops.md`, la carte de résultat et les textes de notification dans `brand.md` : ce plan les appelle sans les réécrire.

Aujourd'hui : jeudi 19 novembre 2026. Sortie payante visée : **lundi 7 décembre 2026**. Repli : **lundi 14 décembre**. Laurène a 15 h par semaine (soirs ~1 h 30, mardi 3 h, samedi et dimanche 3 h chacun) ; Jules prend tout ce qui n'est pas du code.

## 1. Le test réel avant de dépenser

### Test A : la pré-vente fondateurs

Pour un abonnement, le test le moins cher est l'offre fondateurs payée d'avance : **49 €/an pour le couple, 100 places, jusqu'au 31 décembre, encaissé via un lien de paiement Stripe**. Pas de liste d'attente : une carte bancaire.

**Ligne de succès, écrite avant de lancer : 10 couples payants parmi les 50 couples bêta avant le lundi 7 décembre** (objectif des fondateurs, repris dans `pricing.md`). Le lien n'existe qu'une fois l'entité créée et Stripe en mode réel (section 2) ; s'il n'est pas en ligne le lundi 30 novembre, la ligne est mesurée 7 jours après sa mise en ligne, au plus tard le 14 décembre.

**Règle de comparaison avec le panel.** Le panel v2 achète à 17 % ; 10 sur 50 ferait 20 %.
- **10 ou plus** : le réel confirme le panel ; on lance, les 600 € de janvier restent en jeu (décision le 6 janvier).
- **5 à 9** : on lance, mais les 600 € sont gelés tant que le canal qui a amené ces couples n'a pas un coût connu.
- **Moins de 5** : les vrais acheteurs disent non là où le panel disait oui ; on les croit. Retour à `/founder-offer` (mode solo, lettre au partenaire) ou à `/founder-pricing` **avant** le premier euro des 600 €. Le 7 décembre reste (il ne coûte rien), la pub non.

Jules note le profil de chaque couple payant (le panel dit couples « à rituel » et jeunes mamans) pour que `marketing.md` cible juste.

### Test B : le blocage n° 1 du panel

22 refus sur 25 tiennent à « mon partenaire ne le fera jamais ». Seuls de vrais couples tranchent. Sur les 50 couples bêta, dès le 30 novembre :
- **acceptation de l'invitation partenaire : objectif ≥ 30 %** (KPI des fondateurs). En dessous, mode solo et lettre au partenaire passent devant toute brique de janvier ;
- **retour à J1 et J7** après le premier soir à deux. Le board exige un objectif J7 fixé avant le 7 décembre ; les fondateurs ne l'ont pas écrit. Proposition à valider : 50 % des couples en essai reviennent au septième soir, la barre de la complétion du test.

Ces chiffres sont la première condition du board : Laurène les sort de Clarity et Supabase cette semaine.

## 2. Le compte à rebours

**[CC]** = chemin critique, une glissade décale la sortie. L = Laurène, J = Jules.

### Semaine 1 : jeudi 19 → dimanche 22 novembre

| quoi | qui | échéance |
|---|---|---|
| **[CC] Déclarer la micro-entreprise** (guichet unique), pièces selon `ops.md` | J | ven. 20 nov. |
| Chiffres réels du site (Clarity, Supabase), 1 h | L | ven. 20 nov. |
| **[CC] Migration de domaine** préparée : redirections app.myrelation.fr → mylovelab.fr, liens des e-mails et de /duo (soirs jeu., ven.) | L | ven. 20 nov. |
| **Brique 1, Stripe et offre fondateurs** en mode test : Duo 9,90 €/mois et 59 €/an, fondateurs 49 €/an limité à 100, essai 14 jours qui ne démarre que quand les deux ont fait le test, résiliation en un clic (week-end, 6 h) | L | dim. 22 nov. |
| Liste nominative des 50 couples bêta (réseaux des deux écoles, abonnés Instagram, couples « à rituel ») ; relance des 4 praticiens positifs : page partenaire, code ?ref=, Duo offert, « envoyez-nous 2 couples » | J | dim. 22 nov. |

### Semaine 2 : lundi 23 → dimanche 29 novembre

| quoi | qui | échéance |
|---|---|---|
| **[CC] Migration terminée** : plus aucune URL myrelation dans test → compte → invitation → session (lun., mar., 4 h 30) | L | mar. 24 nov. |
| Marketing J−14 : début du calendrier de `marketing.md` | J | lun. 23 nov. |
| **[CC] Suivi SIRET** ; dès réception : compte bancaire pro, puis activation Stripe en mode réel. Ces délais ne dépendent pas des fondateurs : c'est le chemin critique | J | au plus tard ven. 4 déc. |
| Pages légales selon la liste de `ops.md` (CGV, rétractation, garantie 30 jours) ; mise en ligne mer. 25 au soir | J (texte), L (en ligne) | jeu. 26 nov. |
| **Brique 2, mails automatiques** = le mécanisme du lendemain exigé par le board : bienvenue, question du soir par e-mail à 20 h, rappel J−3 avant fin d'essai, confirmation d'annulation (Brevo) ; plus le check-in du soir (week-end, 6 h). Les **sons** sortent de l'avant-lancement : pas sur la boucle, pas le temps | L | dim. 29 nov. |
| **Gel du code** à 22 h : ensuite, corrections de bugs uniquement | L | dim. 29 nov. |
| Bêta : 25 couples inscrits, par messages personnels (les canaux froids ont échoué) | J | dim. 29 nov. |
| Créatrices : 10 contactées (30 % sur 12 mois + un test gratuit à partager en story) ; objectif réaliste : des réponses, pas 10 signatures | J | dim. 29 nov. |

### Semaine 3 : lundi 30 novembre → dimanche 6 décembre

| quoi | qui | échéance |
|---|---|---|
| **Ouverture douce** : 10 couples friends-and-family passent les coutures une par une (test → invitation → compte → essai → session à deux → e-mail du soir), cochées dans `ops.md` | J (suivi), L (correctifs) | mer. 2 déc. |
| Carte « Vos deux regards » et textes de notification de `brand.md` intégrés (3 h) ; manifest PWA le même soir si les correctifs le laissent. **Le web push ne tient pas dans 15 h** : l'e-mail du soir est le rappel de lancement, le push arrive en janvier | L | mar. 1er déc. |
| **[CC] Lien de paiement fondateurs en ligne dès Stripe réel** ; envoi aux couples bêta le jour même : départ du test A | L (lien), J (envoi) | au plus tard ven. 4 déc. |
| Bêta : 50 couples inscrits | J | dim. 6 déc. |
| Praticiens : les 4 positifs actifs (page, code, un couple envoyé) ; les 156 autres relancés avec le test gratuit. L'objectif de 20 actifs passe au 31 janvier : à 4 réponses sur 160, il n'est pas atteignable en 18 jours | J | ven. 4 déc. |
| **GO / NO-GO, vendredi 4 décembre, 19 h** | L + J | ven. 4 déc. |
| Répétition du jour J, déploiement final dim. 18 h, /duo mis à jour (« bêta gratuite » remplacée par l'essai et l'offre fondateurs) | L | dim. 6 déc. |

**Critères du go, vendredi 4 décembre.** Tous les critères durs, sinon no-go.
1. *Dur* : SIRET reçu, compte bancaire ouvert, Stripe activé en mode réel.
2. *Dur* : migration de domaine terminée.
3. *Dur* : invitation, paiement, session partagée et e-mail du soir passés par 10 couples sans correctif ouvert.
4. *Dur* : l'e-mail du soir parti automatiquement à 20 h les 2, 3 et 4 décembre.
5. *Dur* : pages légales en ligne.
6. *Souple* : 30 couples bêta inscrits ; en dessous, on lance mais les 150 € de Noël restent gelés jusqu'à 30.

**Règle du repli.** Pas d'entité au 4 décembre : la sortie glisse au **lundi 14 décembre**, second go/no-go le **vendredi 11 décembre**. On ne lance pas sans entité, même « quelques jours » : condition du board et obligation légale. Au-delà du 14, pas de lancement la semaine de Noël : lundi 4 janvier 2027, offre fondateurs re-datée.

### Du 7 au 31 décembre

Revues J7 (lun. 14 déc.) et J14 (lun. 21 déc.), section 4. Les 150 € de Noël ne partent pas avant le 14 décembre, après 10 couples passés par les coutures (board : aucun euro de pub avant), chaque euro étiqueté par canal, dates dans `marketing.md` (J). Jeudi 31 décembre à minuit : fin de l'offre fondateurs, passage à 59 €/an, compte des places vendues (L). Tout décembre : corrections de bugs seulement (section 5).

## 3. Le jour J : lundi 7 décembre 2026

Hypothèse : Laurène libre avant 8 h, de 12 h à 13 h et après 19 h ; Jules joignable toute la journée. Le code attend un créneau de Laurène ; entre deux, Jules applique les parades du registre des risques de `ops.md`.

| heure | qui | quoi |
|---|---|---|
| 6 h 45 – 7 h 45 | L | Bascule : tarifs et offre fondateurs visibles, « bêta gratuite » retirée. Achat de contrôle à 49 € depuis un compte test (webhook reçu, essai créé dans Supabase, e-mail de bienvenue), puis remboursement. Un lien d'invitation ouvert sur un second téléphone. |
| 7 h 45 | L → J | « C'est ouvert », état des trois contrôles. |
| 8 h 00 | J | Mail de lancement aux couples bêta et à la liste : offre fondateurs, lien de paiement, test gratuit à envoyer au partenaire (texte dans `marketing.md`). |
| 8 h 30 | J | Instagram : post + story avec la carte « Vos deux regards » (`brand.md`), lien vers le test. |
| 9 h – 12 h | J | Messages personnels aux 50 couples bêta et aux 4 praticiens (lien ?ref=). Surveillance Stripe et DM. Pas de code. |
| 12 h – 13 h | L | Point technique : événements Stripe, invitations acceptées, ouvertures du mail. Correctifs urgents seulement. |
| 13 h – 19 h | J | Réponses, relances, créatrices ; note de tout ce qui bloque un couple. |
| 19 h – 20 h | L | Contrôle de la question du soir : contenu, lien, heure. |
| 20 h 00 | auto | **Première question du soir par e-mail** à tous les couples en essai. |
| 20 h – 21 h 30 | L + J | Ouvertures et réponses ; bugs ; chiffres du jour (section 4) ; debrief 15 min, une priorité pour mardi. |

**L'offre du jour** : fondateurs, 49 €/an pour deux, 100 places jusqu'au 31 décembre, satisfait ou remboursé 30 jours, résiliable en un clic. Aucune autre remise.

**Si ça casse** (parades de `ops.md`) :
- *Webhook Stripe muet* (payé, essai non activé) : Jules répond au couple dans l'heure, Laurène active l'essai à la main dans Supabase à 12 h ou 19 h ; plus de deux cas avant midi, Jules retire le lien de paiement, le test gratuit continue.
- *Lien d'invitation cassé* : Jules envoie au partenaire le code à 6 caractères de /duo, valable 7 jours ; Laurène corrige au créneau suivant.
- *E-mail du soir non parti à 20 h* : Jules envoie la question à la main avant 21 h ; mardi, Laurène repasse la tâche planifiée. Pas encore de push : aucun canal à perdre.
- *Site en panne* : retour au déploiement du dimanche 6 ; aucune annonce tant que l'achat de contrôle ne repasse pas.

## 4. Les 30 premiers jours

### Les chiffres de la semaine (Jules, chaque lundi)

| chiffre | source | niveau qui déclenche un changement |
|---|---|---|
| Tests terminés / commencés | Clarity, Supabase | < 50 % : on retravaille le test, pas le reste |
| Invitations acceptées / envoyées | Supabase | < 30 % : mode solo et lettre au partenaire en tête de janvier |
| Essais démarrés (les deux ont fait le test) | Stripe | zéro sur une semaine : la couture invitation → essai est cassée |
| Essais qui atteignent le 7e soir | Supabase | sous l'objectif J7 (proposition 50 %) : le rappel du lendemain devient le chantier de janvier, push en premier |
| Couples payants (cumul) vs seuil de 36 | Stripe | 10 fondateurs au 31 déc. ; 36 (`cfo.md`) est l'horizon, pas la barre du mois |
| Paiements / tests terminés | Stripe ÷ Supabase | < 3 % : retour à l'offre avant la pub |
| Remboursements / paiements | Stripe | > 15 % (haut de la fourchette de `offer.md`) : chercher le motif, suspendre la pub |
| Coût par couple payant, par canal | dépenses étiquetées ÷ couples payants du canal | > 30 € (valeur d'un couple, `cfo.md`) : on coupe le canal ; viser 10 € |

### Les trois revues

**J7, lundi 14 décembre.** Combien de couples payants, dans quel groupe ? Invitation au-dessus de 30 % ? Retour le lendemain du premier soir ? Les 150 € de Noël partent-ils, sur quel canal ? Qu'est-ce qui a cassé le jour J ? Si no-go le 4, cette date devient le jour J et la revue glisse au 21.

**J14, lundi 21 décembre.** Les premiers essais arrivent à échéance : combien convertissent, combien annulent, pourquoi ? Le rappel J−3 est-il parti ? Un canal a-t-il un coût par couple connu et inférieur à 30 € ? Les 4 praticiens ont-ils envoyé un couple chacun ?

**J30, mercredi 6 janvier 2027 : la décision sur les 600 € de janvier.** On dépense si, et seulement si : (1) au moins 10 couples payants fondateurs au 31 décembre ; (2) invitation ≥ 30 % et J7 au-dessus de l'objectif fixé ; (3) remboursements ≤ 15 % ; (4) un canal mesuré sur les 150 € de Noël à moins de 30 € par couple, car les 600 € doivent produire au moins 20 couples payants pour ne pas être perdus (`cfo.md`). Sinon on garde l'argent, on retourne à `/founder-offer` ou `/founder-pricing`, et les 1 000 € de la Saint-Valentin se décident le lundi 8 février sur les mêmes critères. Même jour : la boucle a-t-elle été mesurée sur 50 couples ? Sinon le gel de la section 5 tient.

## 5. Ce qui est gelé

Jusqu'à ce que la boucle **test → Duo → retour le lendemain** soit mesurée sur 50 couples (invitation, essai, J1, J7, paiement), conformément au board, rien de ceci n'est codé ni annoncé : le jeu de cartes-questions, le calendrier des dates, les podcasts, la version anglaise, la carte cadeau Duo (pour la Saint-Valentin seulement si le gel est levé le 6 janvier), les sons, le pack « une dimension » à 14,90 €.

Seules briques autorisées en janvier : celles que les chiffres réclament, le web push si J7 est sous l'objectif, le mode solo et la lettre au partenaire si l'invitation est sous 30 %. Une seule à la fois.

Prochaine étape : `/founder-plan` compile le tout dans le plan d'affaires.
