# MyLoveLab · Business plan

**Verdict: Not yet**

- ✓ Each couple-mois (un mois de Duo payé par un couple, mix mensuel 9,90 € / annuel 59 €) earns 4.22 € before fixed costs (53% contribution).
- ✓ Year 1 operating profit: 4,141 €.
- ✗ 5 of 30 simulated buyers buy (17%, the bar is 25%).

| key number | |
| --- | ---: |
| Price | 7.90 € a couple-mois (un mois de Duo payé par un couple, mix mensuel 9,90 € / annuel 59 €) |
| Profit margin at plan | 47% per couple-mois (un mois de Duo payé par un couple, mix mensuel 9,90 € / annuel 59 €) |
| Break-even | 2 couple-mois (un mois de Duo payé par un couple, mix mensuel 9,90 € / annuel 59 €)s a day |
| Year 1 operating profit | 4,141 € |
| Startup spend | 2,040 € |
| Cash needed before it pays for itself | 2,191 € |
| Startup money earned back | month 9 |
| Buyer panel | 5 buy · 25 pass |

## The idea

- What it is: un SaaS B2C francophone pour les couples (site web, pas d'app mobile) : un test de relation gratuit en porte d'entrée, puis un programme de sessions ludiques quotidiennes (~8 min) pour mieux se comprendre à deux et faire durer la relation. Promesse grand public : « Mieux vous comprendre à deux, en quelques minutes par jour ».
- Who it is for: cible de lancement = femmes de 25 à 35 ans, en couple depuis 2 à 7 ans, qui vivent avec leur partenaire (de l'emménagement au premier enfant), en France. Ensuite : jeunes parents, puis hommes de 30 à 45 ans via le SEO. Pas pour l'instant : couples en crise aiguë, plus de 50 ans. Praticiens (psychologues, thérapeutes de couple, sexologues) = canal de crédibilité et de recommandation (30 % d'affiliation sur 12 mois + Duo offert), pas une source de volume.
- What it sells, at what price: test d'entrée gratuit (option 0,99 € envisagée) ; abonnement Essentiel ~9,90 €/mois ; Premium Duo ~19,90 €/mois (abonnement partagé à deux, profils miroirs). À tester : annuel pour deux à 39–49 €, partenaire invité gratuit ; carte cadeau Duo 3 mois à 49 €. Prix plafond voulu ~10 €/mois pour rester accessible. Contenu : 7 dimensions (Communication et écoute, Attachement et sécurité, Langages d'amour, Gestion des conflits, Intimité et désir, Confiance et soutien, Projet commun), 10 niveaux × 6 sessions par dimension = 420 sessions ; 24 profils relationnels (4 styles d'attachement × 6 patterns) ; score sur 100 par dimension ; gamification (streaks, niveaux, sons). Bases : Gottman, Sue Johnson, Esther Perel, Bowlby/Ainsworth, Chapman, Schnarch, Nagoski, Fraley, Bodenmann (stress dyadique).
- Where and how: en ligne, France (mylovelab.fr, ancien nom MyRelation, migration de domaine prévue). Acquisition : le test gratuit comme aimant (curiosité ou moment de tension), SEO (blog, pages programmatiques par paires de profils), Instagram (2 posts/semaine), affiliation créatrices (30 % sur 12 mois, sans fixe) et praticiens, codes promo et liens ?ref= via Stripe, pixels Meta/TikTok à venir. Stack : Vercel, Supabase, Stripe, Clarity, GA4.
- Budget and constraints: deux cofondateurs étudiants, non rémunérés, aucun salarié. Laurène (produit, dev, contenu) ~15 h/semaine ; Jules (prospection, partenariats, marketing). Budget pub : 150 € vague Noël, 600 € janvier, 1 000 € Saint-Valentin + réinvestissement du CA. Pas de structure juridique créée à ce jour (à régler avant Stripe et commissions). Sortie payante visée lundi 7 décembre 2026 (mi-décembre). Site ouvert depuis l'été 2026, blog, moins de 20 tests passés à mi-septembre, 160 praticiens contactés, 4 réponses positives. Les canaux froids (DM, mails froids, groupes Facebook) ont peu marché. Objectifs avant sortie : 20 praticiens actifs, 10 créatrices affiliées, 50 couples bêta dont 10 fondateurs payants. KPI tunnel : ≥50 % de tests terminés, ≥3 % de paiement, ≥30 % d'invitations du partenaire. Règles éditoriales : pas d'étiquette figée, « sessions ludiques », éviter diagnostic/thérapie/sauver son couple ; ne remplace pas un thérapeute ; violences → 3919.

> **Mise à jour 19/11/2026, après le panel et l'offre v2** (`offer.md`, `pricing.md`) : l'offre vendue n'est plus « Essentiel 9,90 € solo / Premium Duo 19,90 € » mais **un seul produit, le Duo, 9,90 €/mois pour le couple ou 59 €/an**, essai 14 jours conditionné au test des deux partenaires, satisfait ou remboursé 30 jours, offre fondateurs 49 €/an pour 100 couples jusqu'au 31/12. Le reste de ce fichier décrit l'idée telle que présentée au board.

## Summary

**MyLoveLab** (mylovelab.fr) est un site français pour les couples : un test de couple gratuit de 15 minutes, fondé sur la recherche, puis « le Duo », une question ou une session ludique chaque soir, à deux, pour 9,90 € par mois pour le couple ou 59 € par an. Il s'adresse d'abord aux femmes de 25 à 35 ans qui vivent avec leur partenaire depuis 2 à 7 ans, en France. Deux cofondateurs étudiants, Laurène et Jules, non rémunérés, 15 heures par semaine de développement, lancement payant visé le lundi 7 décembre 2026.

### Le verdict : Pas encore

Calculé par l'outil (`compile.py`), pas écrit à la main :
- ✓ Chaque couple-mois laisse **4,22 €** après ses propres coûts (contribution 53 %).
- ✓ L'année 1 fait **4 141 €** de résultat d'exploitation sur 11 101 € de revenus, avec 149 €/mois de frais fixes et personne de payé ; seuil de rentabilité ≈ 36 couples payants ; mise de 2 040 € remboursée au mois 9.
- ✗ **17 % des acheteuses simulées achètent** (5 sur 30), sous la barre de 25 %. L'offre d'origine faisait 0 sur 20.

Ce qui doit changer, et quel skill le change : le taux d'achat, et il ne dépend plus du prix ni de l'essai (réglés par `/founder-offer` et `/founder-pricing`) mais du **partenaire** : 22 refus sur 25 disent « il ne fera jamais sa part ». C'est `/founder-launch` (50 couples réels, taux d'invitation acceptée) et un `/founder-offer` v3 (mode solo en attendant l'autre, lettre au partenaire, premiers jeux légers) qui tranchent. Les projections reposent sur une montée à 220 couples payants en un an, soit 700 à 1 300 tests terminés par mois ; le site en faisait moins de 20 à mi-septembre. Tant que de vrais couples n'ont pas prouvé mieux, le verdict reste Pas encore.

### Où le board et le panel sont d'accord, et où ils divergent

D'accord sur l'essentiel : le besoin est réel, le test gratuit est l'actif (toutes les acheteuses le feraient), la distribution n'est pas prouvée, et le produit vend une habitude quotidienne à deux sur un site web sans app. Le board (2 PASS, 1 FUND IF, 3,7/10) voulait un prix plus haut et une promesse plus forte ; le panel a fixé un plafond de 12 €/mois et préféré un prix **par couple**. La réconciliation : un seul produit, le Duo, 9,90 € pour deux, c'est plus par personne que l'Essentiel supprimé et sous le seuil de rejet. Le board jugeait le marché difficile à joindre ; le panel le confirme autrement : l'acheteuse est joignable, c'est l'utilisateur indispensable, son partenaire, qui ne l'est pas.

### Le plus gros risque et ce qu'on en fait

**Le partenaire ne vient pas.** Réponse : l'essai de 14 jours ne démarre que quand les deux ont fait le test (on ne paie jamais pour un absent), le partenaire fait sa part en 15 minutes sans compte « pour comparer », les premiers soirs sont des jeux, et le marketing s'adresse à lui autant qu'à elle. Mesure : taux d'invitations acceptées ≥ 30 % sur les 50 couples bêta ; en dessous, on ajoute le mode solo avant de dépenser les 600 € de janvier.

Deuxième risque : la concurrence copie vite (Paired est déjà en français, à 6,25 €/mois en annuel). Le créneau est étroit mais vide : bilan + programme par dimensions, en français, sous 10 €, sans app, test gratuit complet et résiliation en un clic, à l'inverse des deux reproches n°1 du marché.

### Ce qu'il faut pour démarrer

- **Cash : ≈ 2 190 €** (1 750 € de pub déjà budgétés + 230 € de marque INPI + deux mois de frais fixes). Pas de salaire : avec 500 €/mois chacun, l'année 1 perdrait 7 900 €.
- **Avant tout encaissement** : une structure juridique (micro-entreprise ou SAS à deux, voir `ops.md`), le SIRET sur Stripe, les CGV, la migration de domaine.
- **Le premier test réel** (`launch.md`) : pré-vente de l'offre fondateurs à 49 €/an auprès des 50 couples bêta, ligne de succès **10 couples payants avant le 7 décembre**.

### La chose à faire cette semaine

Créer la structure juridique sur le guichet unique (c'est le chemin critique du 7 décembre) et envoyer le lien du test à 10 couples amis en demandant au **partenaire** de le faire de son côté : le taux de retour de ces 10 partenaires dira, avant d'écrire une ligne de code de plus, si le Duo peut se vendre.

*Le panel est fait d'acheteuses simulées et les chiffres sont des projections ; ce sont les vrais couples et les vrais devis qui les confirment. Ce document n'est pas un conseil financier, juridique ni fiscal.*

## What the board said

Trois membres, trois lentilles (Offers, Monopoly, Product), un même brief (`board/brief.md`). Les mémos complets sont dans `board/offers.md`, `board/monopoly.md`, `board/product.md`.

### 1. Le vote

**2 PASS, 1 FUND IF. Score moyen : 3,7 / 10** (Offers 4, Monopoly 3, Product 4).

Le board ne finance pas MyLoveLab tel qu'il est documenté aujourd'hui. Aucun membre n'a jugé l'idée mauvaise ni le besoin faux ; tous trois ont jugé que l'entreprise n'a pas encore apporté la preuve qu'elle sait atteindre son acheteuse et la faire revenir. Un PASS est un résultat, pas un échec : il dit ce qu'il reste à prouver, et les trois lentilles sont d'accord sur ce que c'est.

### 2. Les risques soulevés par plus d'un membre (dans l'ordre)

1. **Aucune distribution prouvée** (Offers, Monopoly, Product). Moins de 20 tests passés à mi-septembre, chiffre actuel inconnu, zéro couple payant, canaux froids en échec, 4 praticiens positifs sur 160, 1 750 € de pub sur trois vagues. Les 100 premiers couples payants n'ont pas de chemin décrit ni de coût connu. C'est le risque n° 1 des trois mémos.
2. **Pas de preuve que ça marche** (Offers, Product). Citer Gottman ou Sue Johnson n'est pas une preuve que ces sessions produisent un résultat pour ce couple. Pas d'avant/après, pas de rétention mesurée, pas de garantie. L'acheteuse n'a aucune raison de croire.
3. **L'habitude quotidienne sur un site web, sans app ni notification native** (Offers, Monopoly, Product). Le produit vend « quelques minutes par jour » mais le moment critique, le lendemain matin, n'est pas conçu. Les concurrents sont dans la poche de l'utilisatrice.
4. **Le prix plafond de 10 €/mois comme principe** (Offers, Monopoly). Être moins cher que Paired n'est pas un positionnement ; combiné à 30 % d'affiliation et à un faible volume, la marge par couple ne finance pas la distribution qui manque.
5. **Pas de douve** (Monopoly, implicitement Offers). Base scientifique publique, contenu reproductible avec les mêmes outils d'IA ; rien n'empêche une copie au sixième mois.
6. **Trop de briques pour 15 h/semaine** (Product, Offers). Cartes-questions, calendrier, podcasts, anglais, carte cadeau : tout cela avant que la boucle test → session → retour ne soit mesurée.
7. **Les coutures et le cadre** (Product). Test anonyme → compte → invitation → Stripe → session à deux, plus une migration de domaine et un lancement payant sans entité juridique.

Désaccord à garder : le Product lens croit que la boucle produit peut tenir si elle est resserrée (FUND IF), là où Offers et Monopoly jugent que le marché lui-même (demande latente, acheteuse difficile à joindre) est le problème et que le resserrage du produit ne suffira pas. Les deux lectures sont compatibles : la seconde se tranche avec des chiffres que la première exige aussi.

### 3. Les conditions, fusionnées en checklist

Chaque ligne indique qui la vérifie dans la suite du pack.

- [ ] **Chiffres réels d'aujourd'hui** : tests complétés, comptes créés, invitations partenaire acceptées, retour J1/J7. À fournir par les fondateurs (Clarity, Supabase). Sans eux, aucune autre condition ne peut être validée.
- [ ] **50 couples bêta, dont 10 qui paient sans remise**, avec scores avant/après et rétention à 30 et 60 jours. → `/founder-launch` (le test réel avant de dépenser).
- [ ] **Un canal qui amène des couples payants à un coût connu** (créatrices, praticiens ou pub). → `/founder-marketing`, `/founder-cfo`.
- [ ] **Le prix testé, pas décrété** : Duo à 19,90 €/mois ou plus face à 9,90 €, plafond de 10 € abandonné comme principe, garantie explicite chiffrée. → `/founder-consumer`, `/founder-pricing`, `/founder-offer`.
- [ ] **Un résultat rapide et nommé** : quelque chose que le couple constate et raconte dans les 7 premiers jours, au cœur de la promesse publique. → `/founder-offer`.
- [ ] **Le mécanisme du lendemain** choisi, en place et mesuré sur le web (e-mail, PWA installable, WhatsApp) avec un objectif de retour J7 fixé avant le 7 décembre. → `/founder-ops`, `/founder-launch`.
- [ ] **Une seule boucle avant toute autre brique** : gel de janvier à mars (cartes, calendrier, podcasts, anglais) tant que la boucle n'est pas mesurée. → `/founder-launch`.
- [ ] **Les coutures passées une par une** : invitation, paiement, session partagée, validées par les fondateurs puis par 10 couples bêta avant tout euro de pub. → `/founder-ops`, `/founder-launch`.
- [ ] **Entité juridique créée et migration de domaine terminée** avant tout encaissement. → `/founder-ops`.
- [ ] **Carte complète des concurrents** (apps, jeux, thérapeutes en ligne, contenu gratuit) et réponse à « que reste-t-il si Paired ajoute un test d'attachement en français ? ». → `/founder-competitors`.
- [ ] **Le « moment de tension » comme porte d'entrée vérifié** auprès de femmes du segment, pas supposé. → `/founder-consumer`.
- [ ] **Coût d'acquisition supportable et mois de rétention nécessaires** pour que 600 € de pub en janvier ne soient pas perdus. → `/founder-cfo`.

### 4. La version la plus forte de cette entreprise, vue du board

Ce n'est pas « une app de couple moins chère que Paired ». C'est **le test de couple de référence en français**, gratuit, anonyme, fondé sur la recherche, qui arrive au bon moment (le soir d'une dispute, via Google et un reel de psy) et qui produit en 15 minutes quelque chose que l'on veut montrer à l'autre. Le produit payant est ensuite le **Duo** : deux regards côte à côte, une question du jour, une action à tester ce soir ; vendu plus cher que prévu, à deux, avec une promesse datée et une garantie, et distribué par les praticiens et les créatrices qui y envoient leurs couples. Le mobile se traite par une PWA installable et un rappel quotidien par e-mail ou WhatsApp, pas par une app native. Tout le reste (cartes, calendrier, podcasts, anglais) attend que la boucle test → Duo → retour le lendemain soit mesurée sur 50 couples. Cette version diffère de ce que les fondateurs ont présenté sur trois points : le prix (plus haut, pas plus bas), l'objet vendu (le Duo, pas l'abonnement solo) et la feuille de route (une boucle, pas dix briques).

*Note de la présidence : le brief a été rédigé avant lecture du site. Le site confirme que le test est déjà gratuit, anonyme et sans compte, que le Mode Duo existe déjà en bêta gratuite, et qu'il y a 17 articles de blog, 6 jeux à deux et 18 pages « recherche ». Cela renforce le point 4 (l'actif, c'est le test et le contenu) et le point 6 (beaucoup de briques existent déjà).*

## The competition

Sources publiques uniquement, chaque fait est lié. Limite de la session : aucun site n'a pu être ouvert directement (apps.apple.com, play.google.com, paired.com, Trustpilot, Unobravo, Gottman, Reddit : « could not reach ») ; tout vient d'extraits de recherche. Les prix App Store sont ceux du pays indiqué ; le prix France de Paired n'est pas confirmé. Données complètes : `competitors.csv`.

### 1. Le tableau (du plus direct au moins direct)

| Concurrent | Type | Canal | Prix comparable (mensuel couple) | Ce qu'il vend | Note / avis |
|---|---|---|---|---|---|
| [Paired](https://www.paired.com/frequently-asked-questions) | Direct | App mobile, [EN/FR/DE](https://support.paired.com/en/articles/164634-can-i-use-paired-in-another-language) | 14,99 €/mois ou 79,99 €/an **par couple** ; en euros ([App Store PT](https://apps.apple.com/pt/app/id1469609343)) 14,99 € / 74,99 € | Question du jour gratuite, quiz, jeux, contenus d'experts | 4,7 / 211K ([App Store US](https://heybonds.com/paired-app-review/)) ; 4,6 / 60,2K ([Play](https://apppricinglab.com/app/google_play/com.getpaired.app)) ; 4,56 / 3,1K ([App Store FR](https://worldsapps.com/fr/reviews-paired-couples-relationship)) |
| [Lasting](https://www.choosingtherapy.com/lasting-app-review/) (Talkspace) | Direct | App mobile, anglais seulement | 29,99 €/mois ; 59,99 €/3 mois ; 89,99 €/6 mois | Bilan de santé du couple puis sessions guidées par thème | 4,7 / 25K ([App Store US](https://apps.apple.com/app/id1225049619)) |
| [Couply](https://apps.apple.com/us/app/couply/id1484241314) | Direct | App mobile, anglais | 70,99 €/an (≈ 5,9 €/mois) ([AppShunter](https://appshunter.io/ios/app/1484241314)) | Quiz de personnalité, coach IA, idées de sorties | 4,6 / 256 (App Store US) |
| [Evergreen](https://apps.apple.com/be/app/id1573360122?l=en-gb) | Direct | App mobile, anglais | 49,99 €/an (≈ 4,2 €/mois, App Store BE) ; 9,99 €/mois ([2021](https://appadvice.com/post/use-the-new-app-evergreen-to-help-build-a-better-relationship/1573360122/1435887944)) | Quiz, jeux, conseils, exercices à deux | 4,79 / 62,9K ([marlvel, faible confiance](https://marlvel.ai/api/llm/apps/health-fitness/evergreen-relationship-growth)) |
| [Flamme](https://apps.apple.com/app/id1583601044) (Arya) | Direct | App mobile, anglais | 12,99 €/mois ; 44,99 €/an | Questions quotidiennes, coach IA, dates | 4,8 / 4 avis Product Hunt (mince) |
| [Coral](https://apps.apple.com/app/id1448861466) | Direct | App mobile, anglais | 59,99 €/an ; 12,99 €/mois ([Adapty 2024](https://adapty.io/paywall-library/coral/)) ; partenaire gratuit | Intimité guidée, prompts quotidiens | 4,6 iOS ; 4,1 / 128 Android |
| [Relish](https://www.ryanandalex.com/relish-app-review/) | Direct | App mobile, anglais, [MAJ Android 2021](https://apps.appfollow.io/android/relish-relationship-coaching-couples-self-care/com.hellorelish.relish?country=us) | 99,99 €/6 mois pour deux (≈ 16,7 €/mois) ; coach humain 156 €/mois | Plans personnalisés + coaching 1-1 | n/a |
| [LovBirdz](https://apps.apple.com/FR/app/id6444805675) (Chouic, Nantes) | Direct | App mobile + jeu de cartes, **français** | 6,99 €/mois ; 24,99 €/an ; 4,99 €/sem. (App Store FR) | Jeu de quiz, +800 questions | 4,8 / 573 ([App Store US](https://apps.apple.com/us/app/id6444805675)) |
| [UpLuv](https://apps.apple.com/fr/app/id1629837933?l=fr) | Direct | App mobile, fiche FR (éditeur Chypre) | 59,99 €/an (App Store FR) ; 9,99 €/mois (US) | Quiz, questions, « test d'amour » | 4,63 / 1,6K ([AppGoblin](https://appgoblin.info/apps/1629837933)) |
| [Love Nudge](https://apps.apple.com/be/app/love-nudge/id495326842) | Direct | App mobile, anglais seulement | Achat unique 9,99 € (App Store BE) | Test des 5 langages de l'amour + nudges | 4,6 / ≈18K ([AppFollow](https://apps.appfollow.io/ios/love-nudge/495326842?country=us)) |
| [Between](https://apps.apple.com/app/id458035189) | Direct (faible) | App mobile | Plus 2,99 €/mois ; 24,99 €/an | Messagerie et souvenirs à deux, pas de programme | 4,8 / 21K |
| [Happy Couple](https://apps.apple.com/app/id6446777255) | Direct (faible) | App mobile, [MAJ 2023](https://appgoblin.info/apps/com.hip.happycouple) | Gratuit | Quiz quotidien | n/a |
| [Unobravo](https://www.unobravo.com/fr/therapie-de-couple) | Indirect | Visio, France | 69 €/séance 50 min ; 1re rencontre gratuite | Thérapie de couple en ligne | « Excellent » Trustpilot (non vérifié) |
| [BetterHelp FR](https://www.betterhelp.com/fr/conseils/th%C3%A9rapies/prix-th%C3%A9rapie-en-ligne-tarifs-remboursement-et-crit%C3%A8res-pour-choisir/) | Indirect | Web/app | dès ~45 €/semaine | Thérapie par abonnement | n/a |
| [Thérapie de couple en cabinet](https://goodassur.com/mutuelle-sante/remboursement/psychologue) | Indirect | France | 70–150 €/séance, [non remboursée](https://www.qare.fr/sante/psychotherapie/therapie-de-couple/) | Séances avec thérapeute | n/a |
| [Gottman Connect](https://www.gottman.com/product-category/online-learning/) | Indirect | Web, anglais | Relationship Adviser 139 € ; [Art & Science of Love 169 €](https://www.marriage.com/fr/advice/counseling/online-marriage-course-cost/) | Bilan + programme digital | n/a |
| [Love Intelligence](https://www.letribunaldunet.fr/interviews/couple-celibataire-florence-escaravage-conseils-ete.html) | Indirect | Coaching FR (mail, tel, face à face) | Prix non publié | Programme « Fantastic Couple » | n/a |
| [Social Couples](https://www.achatmoinscher.com/comparateur-de-prix-Jeux-de-societe/social-edition-couples.html), [Vertellis / Osmooz / Dimoi](https://www.topito.com/top-shopping-jeux-societe-couple-coquin) | Indirect | Amazon.fr, boutiques | 12 € à 22,39 € ; dès 19 € ; 19,99 € | Jeux de cartes à questions | n/a |
| [« Les langages de l'amour » (poche)](https://www.fnac.com/n67968/Sante-Bien-etre-Puericulture/Tout-le-Developpement-personnel/Relations-Homme-Femme) | Indirect | Fnac | 7,90 € | Livre best-seller | 5 221 avis Fnac |
| [Tests gratuits en ligne](https://www.marriage.com/fr/quizzes) (psychologies.com « [centaines de tests gratuitement](https://lesenjeux.univ-grenoble-alpes.fr/wp-content/uploads/2025/12/06-TERTRAIS-FLAMAND-MAIGNAN-LesEnjeux-Dossier2025B-web.pdf) », [« test de l'oiseau » TikTok](https://www.parismatch.be/lifestyle/psychosexo/2024/01/10/le-test-de-loiseau-vous-permettrait-de-savoir-en-quelques-instants-si-votre-couple-durera-T42AWHC7IVHXTHWHPSOGWB7UO4/)) | Substitut | Web, TikTok | 0 € | Quiz de compatibilité, scores 0–100 | n/a |
| [Podcasts](https://www.audible.fr/podcast/LEspace-du-Couple/B08K5Y1RL6) (L'Espace du Couple, [Couples en thérapie](https://rephonic.com/podcasts/couples-en-therapie)), comptes Instagram/TikTok | Substitut | Audio, réseaux | 0 € | Conseils de thérapeutes | audiences FR non trouvées |
| En parler aux amis / ne rien faire | Substitut | — | 0 € | Le statu quo | — |

Note : « Couple AI » ne désigne pas un concurrent établi ; le seul match net ([Couple: Rizz & Dating Coach](https://trustmrr.com/startup/couple-ai-chat-advisor?metric=mrr), 3,99 €/sem.) vise les célibataires. **Tous les concurrents directs sont des apps mobiles ; aucun n'est web-first.** Seuls Paired, LovBirdz et UpLuv ont une interface en français.

### 2. Fourchette de prix (abonnement mensuel pour le couple)

- **Plans mensuels** : le plus bas 2,99 € (Between), médiane **12,99 €** (Coral / Flamme), le plus haut 29,99 € (Lasting). Paired est à 14,99 € (≈ 14,99 €).
- **Plans annuels ramenés au mois** (ce que paient la plupart des abonnés) : 2,1 € (LovBirdz) à 6,25 € (Paired 74,99 €/an) ; médiane ≈ 5 €/mois (UpLuv 59,99 €/an, Coral 59,99 €/an).
- Point clé : chez Paired, Evergreen, Coral, Lasting et Relish, **un seul abonnement couvre les deux partenaires** (« [Only one partner needs to subscribe](https://www.paired.com/frequently-asked-questions) »). MyLoveLab à 9,90 € (Essentiel) est au-dessus de tous les annuels mais sous le mensuel de Paired ; **le Duo à 19,90 € serait le plus cher du marché** pour un contenu que les leaders offrent déjà aux deux.
- Les indirects donnent le plafond : une séance de thérapie (69–150 €) = 7 à 15 mois de MyLoveLab.

### 3. Carte de positionnement (texte)

Axe horizontal : **jeu / léger** ⟶ **thérapie / sérieux**. Axe vertical : **prix par mois pour le couple**.

```
 Prix/mois
 30 € |                                              Lasting (EN, app)
      |
 17 € |                                      Relish (EN, app, dormant ?)
 15 € |            Paired mensuel (FR, app)
 13 € |   Flamme (EN)     Coral (EN, intimité)
 10 € |   UpLuv mensuel                    >>> MyLoveLab Essentiel 9,90 € (FR, WEB) <<<
  7 € |   LovBirdz mensuel (FR)
  5 € |   Couply, UpLuv, Coral annuels      Evergreen annuel
  3 € |   Between (messagerie)
  0 € |   Happy Couple, tests gratuits, « test de l'oiseau », podcasts, amis
      +--------------------------------------------------------------------
        Jeu / léger                                     Thérapie / sérieux
        (quiz, questions, Instagram)   (bilan, programme par dimensions, séances)
 Hors cadre : Gottman Connect 139–169 € (achat unique, EN, web) ; Unobravo 69 €/séance ; cabinet 70–150 €.
```

Lecture : la moitié gauche est encombrée et bon marché (quiz en français inclus : LovBirdz, UpLuv). La moitié droite, « programme structuré avec bilan », n'existe qu'en anglais (Lasting, Gottman) et coûte 2 à 3 fois plus. Paired est au centre : rituel quotidien léger, en français, mais sans bilan par dimensions (les utilisateurs Google Play « [demandent des quiz de compatibilité](https://kimola.com/reports/unlock-relationship-insights-paired-app-feedback-report-google-play-en-in-154993) »). Mobile vs web : 12/12 directs sont mobile only.

### 4. Ce que disent les avis (1–3 étoiles d'abord)

**Paired (référence)**
1. *Tout est derrière le paywall* — thème n°1 des avis 1–3★ du secteur, « [Everything Worth Using Is Locked Behind the Paywall (28%)](https://unstar.app/blog/paired-lasting-love-nudge-evergreen-cupla-couples-apps-ranked-2026) », « aimed hardest at Paired ». Avis FR : « [90% des questions nécessites d'avoir un abonnement à 8€/mois](https://worldsapps.com/fr/reviews-paired-couples-relationship) » (2022) ; « [there is only one free question a day unless you pay](https://pookie-app.com/blog/couples-apps-that-are-actually-free/) ».
2. *Essai qui devient abonnement, résiliation pénible* — « [The Free Trial Quietly Became a Subscription (19%)](https://unstar.app/blog/paired-lasting-love-nudge-evergreen-cupla-couples-apps-ranked-2026) » ; Google Play : « [when I went to cancel my subscription, I had to try on several different occasions because they make it very hard to do so](https://play.google.com/store/apps/details?id=com.getpaired.app&hl=en_US) » ; « the only clickable button is "keep my subscription" » (même fiche).
3. *Contenu répétitif / générique* — « [frustrated with the paywall and repetitive content](https://www.onclarity.com/leaderboard/insight/betterhalf) » ; les prompts « get generic and repetitive » ([unstar](https://unstar.app/blog/paired-lasting-love-nudge-evergreen-cupla-couples-apps-ranked-2026)).
4. *Prix jugé élevé* — avis FR : « 15€ par mois » c'est beaucoup ([worldsapps](https://worldsapps.com/fr/reviews-paired-couples-relationship)). Mince (2 avis FR).
5. *Partenaire qui décroche* — un blog concurrent décrit des fils Reddit où « [one partner enthusiastic, the other not opening it](https://nuzzle-landing.pages.dev/blog/best-free-paired-app-alternatives) » ; source intéressée, **mince**, mais cohérent avec l'objectif MyLoveLab de ≥30 % d'invitations.

**Lasting**
1. *Facturation / résiliation* — « [charged £20 despite the listing advertising a 7-day free trial](https://apps.apple.com/gb/app/lasting-marriage-couples/id1225049619) » ; « [charged again after contacting the company](https://appsrankings.com/app/1225049619/lasting-marriage-couples) » ; pas de bouton d'annulation ([App Store 2019](https://apps.apple.com/us/app/lasting-marriage-couples/id1225049619?see-all=reviews)).
2. *Prix monté* — « [used to be free or cheaper and now costs too much](https://www.choosingtherapy.com/lasting-app-review/) » (29,99 €/mois).
3. *Bugs d'inscription et de synchro partenaire* en 2024–2025 ([heybonds](https://heybonds.com/lasting-app-review/)). Mince (résumé secondaire).
4. *Anglais seulement* ([fiche App Store](https://apps.apple.com/app/id1225049619)).

**Couply / Evergreen**
1. *Paywall agressif* — « [aggressive subscription paywalls limit access to core features for free users](https://marlvel.ai/apps/couply-couples-relationship) » ; « [the "free" questions are extremely limited](https://justuseapp.com/en/app/1484241314/couply-couples-relationship/reviews) ».
2. *Synchro / progression perdue* — « [technical glitches cause progress loss and failure to sync quiz completion status](https://marlvel.ai/apps/couply-couples-relationship) » ; même thème secteur : « [sync that breaks between partners](https://unstar.app/blog/paired-lasting-love-nudge-evergreen-cupla-couples-apps-ranked-2026) ».
3. Evergreen : « [mixed feedback… potential held back by functionality and accessibility](https://kimola.com/reports/deep-dive-into-evergreen-app-feedback-analysis-google-play-en-in-154995) », un avis tagué « Subscription Concerns » (août 2024). **Mince.**

**Produits en français (LovBirdz, UpLuv, Love Nudge)**
Aucun avis négatif verbatim en français n'a été trouvé via la recherche ; UpLuv n'a que [3 avis analysés sur JustUseApp FR](https://justuseapp.com/fr/app/1629837933/upluv-couples-games-quiz/reviews) (**mince**). Love Nudge : « [Una pena que no se pueda cambiar el idioma](https://apps.apple.com/es/app/love-nudge/id495326842) » — la langue est un frein réel pour les apps anglophones.

### 5. Le gap

Il existe, et il est étroit : **« le bilan + programme structuré, en français, à moins de 10 €/mois, accessible sans app »**.
- Personne ne vend en français un programme par dimensions avec score et profils : Paired (FR) est un flux de questions sans bilan, et ses utilisateurs réclament des quiz de compatibilité ([Kimola](https://kimola.com/reports/unlock-relationship-insights-paired-app-feedback-report-google-play-en-in-154993)) ; Lasting et Gottman, qui ont le bilan, sont en anglais et à 29,99 €/mois ou 139–169 €.
- Le reproche n°1 du marché est le paywall sur du contenu gratuit vide ; MyLoveLab fait l'inverse : un test complet gratuit en porte d'entrée (à condition que le test livre une vraie valeur, pas un teaser).
- Le reproche n°2 est la résiliation piégeuse : un abonnement Stripe web, résiliable en un clic, est un argument de vente à afficher.
- Le web est à la fois le gap (SEO sur « test de couple », pages par paires de profils, partage du résultat au partenaire par lien — 0 concurrent direct ne le fait) et le risque (pas de notifications natives pour le rituel quotidien ; prévoir e-mail/WhatsApp/PWA).
- Ce que le gap **n'est pas** : un énième quiz ludique (LovBirdz à 2 €/mois en annuel occupe déjà cette case en français), ni un Duo à 19,90 € (les leaders incluent le partenaire).

### 6. La menace

- **Paired** copie le plus vite : déjà en français, 1 M+ installations, « #1 couples app », livre quiz et contenus toutes les semaines ; ajouter un « bilan par dimensions avec score » est une feature, pas un pivot. Il lui manque le web et un prix sous 10 € (l'annuel est déjà à 6,25 €/mois).
- **Chouic (Nantes)** : studio français rodé aux apps de couple ; pourrait greffer une couche « programme » sur LovBirdz et sa distribution (jeu physique en boutique).
- **Plateformes de thérapie (Unobravo, BetterHelp/ReGain)** : peuvent lancer un programme self-service à bas prix en amont de la séance, avec une crédibilité clinique que deux étudiants n'ont pas.
- Parade : vitesse sur le contenu en français (420 sessions, 24 profils), SEO programmatique, et le réseau de praticiens comme caution — la seule chose que Paired ne peut pas acheter en un trimestre.

## The buyer panel

**5 buy · 25 pass** (17% buy) out of 30 simulated buyers. Seed 7, so the same cards can be dealt again.

70 of 100 buyers have no valid answer and are left out: P031 (missing), P032 (missing), P033 (missing), P034 (missing), P035 (missing), P036 (missing), P037 (missing), P038 (missing), P039 (missing), P040 (missing).

These are simulated buyers, not customers. Use this to find objections and weak spots, then confirm the big ones with real people before you spend.

### By segment

| group | buyers | buy rate |
| --- | ---: | ---: |
| Jeune maman ou enceinte (premier enfant, charge mentale, fatigue) | 7 | 43%  (thin) |
| Active installée (CDI, projet d'achat ou de bébé, couple de 4 à 7 ans) | 6 | 17%  (thin) |
| Jeune active en début de carrière (emploi salarié, loyer à deux, pas d'enfant) | 14 | 7% |
| Étudiante ou en reconversion (petit budget, beaucoup de temps en ligne) | 3 | 0%  (thin) |

### By buying behaviour

| group | buyers | buy rate |
| --- | ---: | ---: |
| Fan de rituels à deux | 4 | 100%  (thin) |
| Lectrice psycho | 6 | 17%  (thin) |
| Curieuse des tests | 8 | 0% |
| Moment de tension | 4 | 0%  (thin) |
| Chasseuse de bons plans | 4 | 0%  (thin) |
| Partenaire réticent | 2 | 0%  (thin) |
| Déjà abonnée ailleurs | 2 | 0%  (thin) |

### By income

| group | buyers | buy rate |
| --- | ---: | ---: |
| 23,000 € to 29,000 € | 9 | 22% |
| 29,000 € and up | 11 | 18% |
| under 23,000 € | 10 | 10% |

### Why they pass

| reason | buyers | in their words |
| --- | ---: | --- |
| habit | 16 | "Le test gratuit, je le ferais ce soir, surtout avec Gottman et l'ECR-R cités, ça me parle. Mais le Duo ne démarre que si mon copain fait le test et répond à une question chaque soir, et je le connais : il va dire oui, oublier, et au bout de trois rappels ce sera moi qui le relance, ce qui est exactement ce que je ne veux pas." (P001) · "Le test gratuit, je le fais direct, j'envoie le lien à mon copain et je partage sûrement le résultat « Vos deux regards » en story. Mais payer 9,90 € par mois pour un site de questions du soir, non : j'ai jamais payé derrière un test et je vois pas pourquoi je commencerais là." (P002) |
| other | 5 | "Le test gratuit, je le ferais sûrement un soir à 23h après une dispute, pour voir. Mais le Duo ne sert à rien si mon copain ne fait pas sa part, et lui, il n'ouvre même pas les reels que je lui envoie, alors un test de 15 minutes puis une question tous les soirs, je n'y crois pas." (P003) · "Le test gratuit, je le fais ce soir sur le canapé, et les sources (Gottman, ECR-R) me rassurent vraiment. Mais le Duo ne démarre que si mon copain fait le test de son côté, et lui, il est sur sa manette : le lien va rester dans WhatsApp sans réponse, donc je n'arrive jamais à l'étape où on paie." (P008) |
| trust | 2 | "Je ferais le test gratuit un soir après une dispute, c'est sûr, mais payer 9,90 € par mois pour qu'un site nous pose une question chaque soir, non. Avec le bébé et 22 000 € par an, je n'ai ni l'énergie ni l'envie de confier mon couple à une appli, et de toute façon il ne fera jamais sa partie du test." (P004) · "Je ferais le test gratuit un soir après une dispute, parce que c'est gratuit et que ça répond tout de suite, mais passer à 9,90 € par mois pour une marque que je ne connais pas, qui n'est même pas encore lancée, et qui demande que mon copain fasse le test de son côté, non. Le soir où ça va mal il ne cliquera pas sur mon lien, et une fois calmés on oublie." (P029) |
| timing | 1 | "Je tombe dessus à 23h après une engueulade, je fais le test gratuit toute seule, j'ai mon score et mon style d'attachement, et là il faudrait que j'envoie un lien à mon copain qui boude dans le salon. Le lendemain la dispute est passée, le lien n'est jamais parti, et une question tous les soirs pendant un an ce n'est pas ce que je cherchais ce soir-là." (P018) |
| need | 1 | "Je ferais le test gratuit par curiosité, peut-être même les 14 jours d'essai, mais je résilierais avant la fin : une question le soir sur le téléphone ne va pas changer qui fait la vaisselle ni qui pense aux courses, et c'est ça nos disputes." (P021) |

### Why they buy

| reason | buyers | in their words |
| --- | ---: | --- |
| habit | 4 | "C'est exactement le genre de petit rituel du soir que j'adore, ça ressemble à un jeu de cartes couple et pas à une thérapie, et 9,90 € pour deux c'est le prix d'un paquet de couches. Je fais le test gratuit, je lui envoie le lien, et si on tient les 14 jours je prends le mois, pas l'année." (P005) · "C'est exactement le genre de petit rituel du soir qu'on aime, et 9,90 € pour nous deux c'est moins qu'un jeu de cartes. Je fais le test gratuit, on essaie les 14 jours, et si ça nous fait rire deux minutes avant de dormir avec le bébé, je prends le mois." (P006) |
| need | 1 | "Depuis le bébé on ne se parle plus que de couches et de biberons, et un truc qui cite Gottman et l'ECR-R au lieu de me vendre du développement perso en rose, ça me parle. Je ferais le test gratuit d'abord, et à 49 € l'année pour nous deux, moins qu'une séance de psy, je prendrais l'offre fondateurs si l'essai tient ses promesses." (P019) |

### What would flip a no

- Qu'il fasse le test de son côté sans que j'insiste, et qu'on tienne les 14 jours d'essai à deux sans que je doive le pousser. Là je prendrais l'offre à 49 €/an sans hésiter.
- Si après les 14 jours on avait vraiment pris le pli à deux et qu'il y avait un tarif genre 3-4 € par mois ou 29 € l'année, je pourrais me laisser tenter.
- Que ce soit lui qui ait fait le test de son côté et qui m'envoie le lien, ou que je voie sur « Vos deux regards » quelque chose qui le fasse réagir vraiment, pas juste des pourcentages.
- Qu'il fasse le test de lui-même et qu'il me dise qu'il a envie de continuer les 14 jours, sans que j'aie à insister.
- Qu'il fasse le test de son côté sans que je le relance, et qu'on arrive au bout des 14 jours en ayant fait au moins la moitié des soirs ; là je prendrais l'offre fondateurs à 49 € sans hésiter.
- Que mon copain fasse le test de lui-même après avoir vu mes résultats, ou que je puisse continuer seule avec mon portrait d'attachement et des sessions solo pendant qu'il se décide.
- Que ce soit lui qui fasse le test le premier et qui me propose le Duo, pas moi qui doive encore le relancer.
- Si pendant l'essai on faisait vraiment les sessions à deux sans que je doive le relancer, et qu'il y avait un code promo ou le tarif fondateurs encore valable au moment où je me décide.
- Si mon copain accroche vraiment pendant les 14 jours et que c'est lui qui me relance le soir pour faire la question, là je prendrais l'offre à 49 € l'année pour nous deux.
- Que ce soit lui qui propose, ou au moins qu'il fasse le test de son côté sans que j'aie à insister ; s'il le fait et qu'il accroche sur les deux semaines gratuites, 49 € pour l'année à deux ça passe.
- Un achat unique autour de 20 € pour une boîte de sessions ludiques à faire à deux (comme un jeu de cartes, mais sur le téléphone), sans abonnement ni notification quotidienne.
- Un achat unique, genre 15 à 20 € une fois pour tout débloquer, comme un jeu de cartes qu'on garde, plutôt qu'un abonnement.

Buyers say they would buy **1.0 times** in the first month on average.

30 buyers gave all four price answers. Run founder-pricing's van_westendorp.py on the answers folder.

## Pricing

Sources : `pricing-curve.md` (20 réponses de prix du panel v1, offre à 9,90 € solo / 19,90 € Duo), `competitors.md`, `numbers.json` passé dans l'outil du CFO à quatre prix. Les réponses de prix viennent d'acheteuses simulées : elles servent à choisir quoi tester, pas de preuve.

### 1. Ce que les acheteuses ont dit (Van Westendorp, 20 réponses, en €/mois)

| point | prix | sens |
|---|---:|---|
| PMC | 3,02 € | en dessous, « trop bon marché pour être sérieux » |
| OPP | 3,04 € | le moins de résistance dans les deux sens |
| IPP | 6,02 € | autant trouvent que c'est une bonne affaire que cher |
| PME | 12,03 € | au-dessus, trop de refus |

Fourchette acceptable : **3 € à 12 € par mois**. Médianes : trop bon marché 2 €, bonne affaire 5 €, cher 12 €, trop cher 20 €. Le 9,90 € solo est dans la fourchette, dans son tiers haut. **Le Duo à 19,90 € est au-dessus du seuil de rejet** (PME 12 €), et c'est précisément le plan que les acheteuses considèrent, puisqu'aucune ne voit l'intérêt de payer seule pour un rituel à deux. En re-test (panel v2, prix 9,90 € pour deux), les réponses restent dans la même zone : bonne affaire 4–5 €, cher 10–12 €, trop cher 15–20 € ; une acheteuse a répondu en annuel (bonne affaire 49 €, cher 79 €, trop cher 120 €).

### 2. Ce que les concurrents facturent (pour le couple, un seul abonnement)

| | mensuel | annuel ramené au mois |
|---|---:|---:|
| Paired (FR, app) | 14,99 € | 6,25 € (74,99 €/an) |
| UpLuv (fiche FR) | 9,99 € | 5,00 € (59,99 €/an) |
| LovBirdz (FR, Nantes) | 6,99 € | 2,08 € (24,99 €/an) |
| Coral / Flamme (EN) | 12,99 € | 3,75–5 € |
| Evergreen (EN) | — | 4,17 € (49,99 €/an) |
| Lasting (EN, le plus proche du « bilan + programme ») | 29,99 € | 15 € (89,99 €/6 mois) |
| Gottman Connect (EN, web) | achat unique 139–169 € | — |
| Thérapie de couple (France) | 60–150 € la séance | — |

Lecture : les leaders incluent le partenaire dans un seul abonnement ; la médiane des mensuels est ≈ 13 €, celle des annuels ≈ 5 €/mois. Un Duo à 19,90 € serait le produit le plus cher du marché grand public ; un Essentiel « par personne » n'a pas d'équivalent chez les leaders.

### 3. Ce dont l'entreprise a besoin (outil du CFO, unité = couple-mois, coûts en % recalculés à chaque prix)

| prix du couple-mois | contribution | marge au plan (300 couples) | seuil de rentabilité | profit an 1 | retour sur la mise |
|---:|---:|---:|---:|---:|---|
| 4,90 € (annuel seul à 59 €) | 2,59 € (53 %) | 43 % | 2 /jour ≈ 59 couples | 1 821 € | pas dans l'année |
| 7,90 € (mix 60 % mensuel / 40 % annuel) | 4,35 € (55 %) | 49 % | 2 /jour ≈ 35 couples | 4 295 € | mois 9 |
| 9,90 € (mensuel seul) | 5,52 € (56 %) | 51 % | 1 /jour ≈ 28 couples | 5 939 € | mois 8 |
| 12,90 € | 7,30 € (57 %) | 53 % | 1 /jour ≈ 21 couples | 8 440 € | mois 7 |

Les coûts fixes sont de 149 €/mois et les fondateurs ne se paient pas : tout prix au-dessus de 5 € couvre les frais dès 30 à 60 couples. Le prix ne décide pas de la survie ; le volume, oui. Ce que le prix décide, c'est le coût d'acquisition supportable (voir `marketing.md`) et la crédibilité.

### 4. Décision

**Le prix : le Duo à 9,90 €/mois pour le couple, ou 59 €/an pour le couple.** Un seul produit, un seul paiement, deux comptes.
- Dans la fourchette du panel (3–12 €), au-dessus du point d'indifférence (6 €) pour ne pas ressembler à un quiz, sous le seuil de rejet (12 €).
- Sous le mensuel de Paired (14,99 €) et au-dessus de son annuel (6,25 €/mois) : le bilan et le programme par dimensions justifient l'écart face à un flux de questions ; l'annuel à 59 € (4,92 €/mois) s'aligne sur UpLuv et Coral.
- Contribution 5,52 € par couple-mois au mensuel, 2,59 € à l'annuel ; marge au plan 49–51 % en mix. Le plafond « 10 €/mois » des fondateurs est respecté mais pour deux personnes, pas une : c'est la réponse du panel (« 10 € chacun, seule non »).
- Le plan Essentiel solo à 9,90 € est retiré : aucune acheteuse n'en a voulu, et il brouille l'offre (Product lens : couper).

**L'échelle**
| rang | offre | prix | pourquoi monter |
|---|---|---:|---|
| Gratuit | Le test, « Vos deux regards », 3 jeux à deux | 0 € | la porte d'entrée, complet, pas un teaser (reproche n°1 du marché : le paywall vide) |
| Bon | Duo mensuel | 9,90 €/mois pour deux | essai 14 jours quand les deux ont fait le test, résiliable en un clic |
| Mieux | Duo annuel | 59 €/an pour deux (≈ 4,92 €/mois) | 5 mois offerts ; le choix des « chasseuses de bons plans » et des cadeaux |
| À tester plus tard | Pack une dimension (10 niveaux, à vie) | 14,90 € une fois | demandé par 5 acheteuses sur 20 (« un paiement unique plutôt qu'un abonnement ») ; à ne lancer que si la rétention mensuelle est mauvaise, car il cannibalise l'annuel |

**L'offre d'ouverture** : « Offre fondateurs », 49 €/an pour les 100 premiers couples, jusqu'au 31 décembre 2026, prix garanti tant que l'abonnement reste actif. Vraie rareté (100 places, date), un seul rabais, pas de « -30 % » récurrent qui apprendrait à attendre les promos. La Saint-Valentin se fait ensuite avec la carte cadeau Duo (59 €, l'annuel au prix normal), pas avec une remise.

**À tester avec de vrais acheteurs**
1. Deux pages de paiement en A/B sur le site dès la bêta : Duo à 9,90 €/mois vs 12,90 €/mois (annuel 59 € vs 79 €). Critère : revenu par visiteur de la page, pas le taux de clic. Au moins 200 visiteurs par branche avant de conclure.
2. Pré-vente de l'offre fondateurs (49 €/an) auprès des 50 couples bêta : ligne de succès 10 couples payants avant le 7 décembre (objectif des fondateurs). En dessous de 5, revenir à l'offre avant de dépenser les 600 € de janvier.

### 5. Les objections de prix du panel, mot pour mot (pour le marketing)
1. « 9,90 € par mois pour un site c'est le prix de Netflix, que je regarde tous les soirs, lui. » (P002)
2. « 19,90 € par mois pour la version à deux, avec le bébé et mon salaire, c'est le prix des couches du mois ; et la version à 9,90 € toute seule, ça n'a aucun sens pour un rituel de couple. » (P006)
3. « Un vrai essai gratuit du Duo d'une quinzaine de jours après le test, ou un format à acheter une fois (genre un pack de niveaux à 15–20 €, comme un jeu de cartes) plutôt qu'un mensuel. » (P006, ce qui la ferait changer d'avis)

Le prix a changé par rapport à `idea.md` : `numbers.json` est à jour (prix de base 7,90 € = mix estimé), le CFO est relancé dans `cfo.md`.

## The offer

Méthode : la lentille Offers (`../jakeschincariol/founder-skill/skills/founder-board/lenses.md`, résumé du cadre de *100 €M Offers*, jamais présenté comme les mots de l'auteur). Matière première : `panel-v1/results.md` (0 achat sur 20), `competitors.md` (reproches du marché), `board.md` (conditions), `numbers.json` (ce que chaque brique coûte).

### 1. Ce que vendait l'offre d'origine (pitch v1, `pitch-v1.md`)
Test gratuit → Essentiel 9,90 €/mois (une personne) ou Premium Duo 19,90 €/mois, sans essai, site web sans appli. Résultat : 0 achat sur 20. Les acheteuses ont adoré le test et refusé l'abonnement, pour quatre raisons qui reviennent dans 20 réponses sur 20.

### 2. La liste des problèmes (dans les mots des acheteuses)

**Avant d'acheter**
1. « Mon copain ne fera jamais ça avec moi » / « il n'ouvre même pas les reels que je lui envoie » (12 réponses sur 20).
2. « 9,90 € par mois pour un site, c'est le prix de Netflix » ; « 19,90 € c'est le prix des couches du mois ».
3. « Je ne m'abonne jamais derrière un test », « on n'a pas de problème, pourquoi payer ».
4. « Pas d'essai gratuit : je dois payer avant de savoir si on tient le rythme ».
5. « C'est quoi cette marque, jamais entendu parler » ; « Gottman cité pour faire sérieux ».
6. « Je ne veux pas confier ma vie de couple à un site ».
7. « Une appli ne remplace pas un vrai psy ».
8. « La version à 9,90 € toute seule n'a aucun sens pour un rituel de couple ».

**Pendant**
9. « Pas d'appli, pas de notification : j'oublie au bout de trois jours » (8 réponses).
10. « 8 minutes par jour, j'ai déjà abandonné Duolingo » ; « avec le bébé je n'ai pas l'énergie ».
11. « Je serai la seule à faire l'effort, et je vais le relancer tous les soirs ».
12. « Une question le soir ne change pas qui fait la vaisselle » (le vrai sujet : charge mentale).
13. « Envoyer un lien "fais ce test" juste après une dispute, impossible ; le lendemain c'est passé ».
14. « Les premières questions doivent être légères, pas un interrogatoire de psy » (pour le partenaire).

**Après**
15. « Encore un abonnement que je vais oublier de résilier » (reproche n°2 du marché, `competitors.md`).
16. « Le contenu va se répéter » (reproche n°3 du marché, Paired).
17. « Si on se sépare, qu'est-ce qui reste ? » (données).
18. « Je préférerais payer une fois, comme un jeu de cartes » (5 réponses).
19. « Mes réponses détaillées, est-ce qu'il les voit ? ».
20. « Et si ça ne nous apporte rien ? » (pas de garantie).

### 3. Les solutions, notées et triées

| problème | solution | valeur acheteuse (1–5) | coût de livraison (1–5) | gardée ? |
|---|---|:-:|:-:|:-:|
| 1, 11, 13 | **Le partenaire fait le test seul, sans compte, depuis un lien** ; « Vos deux regards » n'apparaît que quand les deux ont fini | 5 | 1 (existe déjà sur le site) | oui, cœur |
| 1, 4, 11 | **L'essai de 14 jours ne démarre que quand les deux ont fait le test** : on ne paie jamais pour un partenaire absent | 5 | 2 (logique Stripe trial + condition) | oui |
| 2, 8 | **Un seul produit : le Duo, un paiement pour deux**, 9,90 €/mois ou 59 €/an ; l'Essentiel solo disparaît | 5 | 1 | oui |
| 9, 10 | **Installable sur l'écran d'accueil (PWA) + notification du soir avec la question dedans**, ou le même rappel par e-mail ; la question du jour se fait en deux minutes depuis la notification | 5 | 3 (service worker, web push, Brevo) | oui |
| 14 | **Premiers jours légers** : jeux (« Tu préfères », « Qui de nous deux ») avant les sessions de fond | 4 | 1 (jeux existants) | oui |
| 5, 7 | **Chaque session cite sa source** (déjà le cas), + page praticiens partenaires visible | 3 | 1 | oui |
| 15 | **Résiliation en un clic depuis le compte**, rappel 3 jours avant la fin de l'essai (obligation légale et argument de vente) | 4 | 1 | oui |
| 20 | **Satisfait ou remboursé 30 jours**, sans question | 4 | 2 (coût estimé : 5 % de remboursements × 9,90 € ≈ 0,50 €/couple-mois le premier mois) | oui |
| 3, 5 | **Offre fondateurs** : 49 €/an pour les 100 premiers couples jusqu'au 31/12, prix garanti ; vraie rareté, datée | 4 | 1 (manque à gagner 10 €/an/couple) | oui |
| 12 | Sessions « charge mentale et partage des tâches » visibles dès la page d'accueil (dimension Confiance et soutien) | 4 | 2 (contenu existant à mettre en avant) | oui |
| 18 | Pack une dimension à 14,90 € une fois | 3 | 2 | plus tard (cannibalise l'annuel, voir `pricing.md`) |
| 1 | **Mode solo** : continuer seule avec son portrait et des sessions solo pendant que l'autre se décide | 4 | 2 (le programme solo existe déjà) | **à ajouter en v3** : demandé par 3 acheteuses du re-test |
| 1 | « Lettre au partenaire » : un message pré-écrit, léger, qui invite l'autre à faire le test « pour comparer », sans « on a un problème » | 4 | 1 | **à ajouter en v3** |
| 16 | 420 sessions écrites, 7 dimensions : dire le nombre | 2 | 1 | oui (preuve de volume) |
| 17, 19 | Ce qui reste privé, délier en un clic (déjà sur /duo) | 3 | 1 | oui |
| 9 | Appli native iOS/Android | 5 | 5 (hors de portée à 15 h/semaine) | non |
| 10 | Rappel par SMS/WhatsApp | 4 | 4 (0,03–0,05 € par message × 2 personnes × 30 jours ≈ 2–3 €/couple-mois, un tiers du prix) | non pour l'instant ; e-mail et web push d'abord |

### 4. La pile (ce que voit l'acheteuse)

**Le cœur** : *Le Duo MyLoveLab*. Deux comptes reliés, un seul paiement. Le résultat vendu : « vous comprendre à deux, deux minutes par soir », pas « 420 sessions ».

**Les bonus** (chacun tue une objection)
1. *Vos deux regards* : le test fait chacun de son côté, les scores côte à côte, uniquement quand les deux ont fini (objection 1, 13).
2. *La question du soir dans la notification* : deux minutes, sans ouvrir le site (objection 9, 10).
3. *14 jours offerts, qui ne démarrent que quand vous êtes deux* (objection 4, 11).

**La garantie** : satisfait ou remboursé 30 jours, résiliation en un clic, rappel avant la fin de l'essai. Coût modélisé : à 5 % de remboursements, 0,50 € par nouveau couple, soit 1 % du revenu annuel d'un couple ; à 15 %, 1,50 €. Supportable (contribution 4,22 € par couple-mois, `cfo.md`).

**La rareté** : offre fondateurs, 100 couples, 49 €/an, jusqu'au 31 décembre 2026, prix garanti tant que l'abonnement est actif. Après : 59 €/an. Pas de compte à rebours artificiel, pas de « -30 % Saint-Valentin » (la Saint-Valentin se vend avec la carte cadeau au prix normal).

**Le nom** : « Le Duo » (le produit) et « Offre fondateurs » (le lancement). Pas « Premium », pas « Essentiel ».

### 5. L'équation de valeur, avant / après (1–10)

| | v1 | v2 | ce qui bouge |
|---|:-:|:-:|---|
| Résultat rêvé | 6 | 7 | « vous comprendre à deux » reste le même rêve ; « Vos deux regards » le rend visible |
| Probabilité perçue | 2 | 4 | sources citées, essai gratuit, garantie ; toujours pas de preuve sociale (marque inconnue) |
| Temps avant résultat | 4 | 7 | le premier résultat (les deux regards) arrive le soir même, pas au niveau 10 |
| Effort et sacrifice | 2 | 5 | 2 minutes depuis la notification au lieu de 8 minutes sur un site ; mais l'effort n°1, convaincre le partenaire, reste à la charge de l'acheteuse |

### 6. Le re-test

Même seed, mêmes cartes. `pitch.md` = v2, `pitch-v1.md` = v1.

| | v1 | v2 |
|---|:-:|:-:|
| acheteuses interrogées | 20 | 30 (dont les 20 de la v1) |
| achètent | **0 (0 %)** | **5 (17 %)** ; sur les 20 cartes communes : 4 (20 %) |
| qui achète | personne | 4 « fans de rituels à deux » sur 4 ; 3 jeunes mamans sur 7 ; 1 lectrice psycho |
| objection n°1 | prix + partenaire + pas d'app (ex æquo) | **le partenaire** : 22 réponses sur 25 refus en dépendent |
| objections tombées | « pas d'essai », « 19,90 € », « je paie seule », « pas de rappel » ont disparu ou presque | |
| réponses de prix | fourchette 3–12 €/mois | fourchette 3–12 €/mois, inchangée (`pricing-curve-v2.md`) |

Ce que dit le re-test : l'offre a réglé le prix, l'essai et le rappel. Elle n'a pas réglé le problème de fond, qui n'est pas une objection d'offre mais une objection de **marché** : l'acheteuse est la femme, l'utilisateur indispensable est l'homme, et elle ne croit pas qu'il viendra. Les 5 qui achètent sont celles dont le couple a déjà un rituel à deux. Les 25 autres disent presque toutes la même phrase : « qu'il fasse le test de son côté sans que j'insiste, et je prends l'offre à 49 € ».

Conséquences pour la suite :
- `/founder-marketing` doit vendre **au partenaire** autant qu'à l'acheteuse : un test qui se fait en 15 minutes seul, sans compte, « pour comparer », avec des premiers jeux légers ; et chercher les couples qui ont déjà un rituel (jeux de cartes, questions du soir).
- v3 à tester avec de vrais couples : le **mode solo** (continuer seule pendant que l'autre se décide, demandé 3 fois) et la **lettre au partenaire**.
- Le taux de 17 % est sous la barre de 25 % du compilateur de plan : le verdict sera « Pas encore » tant que de vrais couples n'ont pas montré mieux.

### Règles tenues
Toutes les promesses sont livrables avec ce qui existe sur le site (test sans compte, Duo, jeux) plus trois briques : essai conditionnel Stripe, PWA + web push, e-mails de rappel. Pas de faux avis, pas de faux compte à rebours. La garantie et la résiliation suivent le droit de la consommation français (information précontractuelle, rappel avant reconduction) : à faire relire, pas un conseil juridique.

## The numbers

Tout chiffre ci-dessous vient de `numbers.json` passé dans l'outil (sortie brute plus bas) ou d'un what-if relancé avec le même outil. Les sources et les estimations sont dans `cfo-sources.md`. Base : micro-entreprise en franchise de TVA, fondateurs non payés, prix moyen 7,90 € par couple-mois (mix estimé mensuel 9,90 € / annuel 59 €). Pas un conseil comptable, fiscal ni juridique : un expert-comptable doit valider la structure, les cotisations et la TVA avant le premier encaissement.

### La marge
- **Contribution : 4,22 € par couple-mois (53 %)** après Stripe (0,37 €), affiliation moyenne (1,19 €), cotisations sociales micro 2026 (2,02 €) et e-mails (0,10 €).
- **Marge au plan (300 couples actifs) : 47 %.** Coûts fixes 149 €/mois seulement, parce que personne n'est payé.
- **Seuil de rentabilité : 2 couple-mois par jour, soit ≈ 36 couples payants.** En dessous, le site perd ~150 €/mois.

### La ligne à surveiller : le volume, pas le prix
- Le what-if « prix −10 % » coûte 1 100 € sur l'année ; « volume −20 % » en coûte 1 200 € ; « volume −50 % » ramène le profit an 1 à 1 176 € et la mise n'est pas remboursée dans l'année.
- La montée en charge (10 couples en décembre → 220 en novembre 2027) suppose 20 à 40 nouveaux couples payants par mois avec 15 % de churn. Le panel v2 achète à 17 % (borne haute, simulée) et l'objectif réel des fondateurs est 3 % de paiement sur les tests terminés : il faut donc **≈ 700 à 1 300 tests terminés par mois** pour tenir la courbe, contre moins de 20 à mi-septembre. C'est l'hypothèse qui décide de tout ; les 50 couples bêta diront si elle tient.
- Deuxième ligne : **l'affiliation**. Si 100 % des clients viennent par des créatrices ou des praticiens à 30 %, la contribution tombe à 3,17 € (40 %), la marge au plan à 34 %, le profit an 1 à 2 665 €. Supportable, mais 30 % sur 12 mois est généreux pour un prix de 7,90 € : prévoir de passer à 30 % sur 6 mois ou 20 % sur 12 mois une fois les 10 premières affiliées signées.
- Troisième ligne : **les cotisations**. Le taux micro BNC 2026 est de 25,6 % (21,2 % si l'activité est classée BIC) et l'ACRE n'exonère plus que 25 % la première année et n'est plus automatique (`ops.md`) : le classement BNC/BIC vaut ± 0,35 € par couple-mois, à trancher avec l'URSSAF et un comptable avant le 7 décembre.

### Cash
- **Cash nécessaire avant que ça se paie tout seul : ≈ 2 190 €**, atteint au mois 2 ; c'est la mise de départ (1 750 € de pub + 230 € INPI + 60 €) plus deux mois de frais fixes.
- Mise remboursée au **mois 9** (août 2027). Profit an 1 : 4 141 € sur 11 101 € de revenus ; 2 101 € après la mise.
- Ce que le modèle ne paie pas : le temps des fondateurs. Avec 500 €/mois chacun, le seuil passe à 10 couple-mois/jour (≈ 300 couples), la marge au plan à 5 %, et l'année 1 perd 7 859 €. **MyLoveLab n'est pas encore une entreprise qui rémunère ; c'est un projet qui s'autofinance à partir de 36 couples.**

### Trois façons d'améliorer la marge (chiffrées avec l'outil)
1. **Pousser l'annuel au lieu du mensuel ne l'améliore pas** : à 4,90 € de prix moyen (100 % annuel), le profit an 1 tombe à 1 821 €. L'annuel sert à la trésorerie et à la rétention, pas à la marge. Garder le mensuel visible.
2. **Monter le mensuel à 12,90 €** (prix moyen ≈ 9,90 €) : contribution 5,52 €, profit an 1 5 939 €, +1 700 €. À tester en A/B (`pricing.md`), dans la fourchette du panel.
3. **Plafonner l'affiliation à 6 mois** : si la moitié des clients sont affiliés, la commission moyenne passe de 15 % à ~7,5 % après le premier semestre, soit +0,60 € par couple-mois, ≈ +800 € sur l'année à volume égal.

### Les conditions du board sur l'argent
- « Coût d'acquisition supportable » : avec 4,22 € de contribution et 7 mois de rétention moyenne (churn 15 %), un couple vaut ≈ 30 € de contribution. **Le maximum à payer pour un couple payant est 30 € ; viser 10 €.** À 3 % de paiement, cela veut dire au plus 0,90 € par test terminé, 0,30 € visé. Les 600 € de janvier doivent donc produire au moins 20 couples payants pour ne pas être perdus, 60 pour être rentables (`marketing.md`).
- « Entité juridique avant encaissement » : non chiffrée ici, la micro-entreprise est gratuite à créer ; voir `ops.md`.
- « Le prix testé, pas décrété » : fait, `pricing.md`.

### Sortie de l'outil
## Unit economics: MyLoveLab (abonnement couples, France) — base : micro-entreprise en franchise de TVA, prix TTC = HT

Every number below comes from the input file. Nothing is looked up or guessed.

### One couple-mois (un mois de Duo payé par un couple, mix mensuel 9,90 € / annuel 59 €)

| line | per couple-mois (un mois de Duo payé par un couple, mix mensuel 9,90 € / annuel 59 €) |
| --- | ---: |
| Price | € 7.90 |
| Frais Stripe (1,5 % + 0,25 € par paiement carte UE, sur 7,90 €) | -€ 0.37 |
| Commission d'affiliation (30 % sur 12 mois, estimée sur 50 % des clients = 15 % en moyenne) | -€ 1.19 |
| Cotisations sociales micro-entreprise BNC 2026 (25,6 % du CA encaissé, à vérifier ; 21,2 % si BIC) | -€ 2.02 |
| E-mails de rappel et transactionnels (≈ 70/mois pour deux comptes) | -€ 0.10 |
| **Contribution** (what each couple-mois (un mois de Duo payé par un couple, mix mensuel 9,90 € / annuel 59 €) leaves to pay the fixed costs) | **€ 4.22** (53%) |

### The margin that matters

Fixed costs: € 149 a month (Vercel Pro (hébergement, usage commercial) € 18, Supabase Pro (base, auth, sauvegardes) € 23, Outil d'e-mailing (Brevo, gratuit sous 300 e-mails/jour puis Starter ≈ 7 € HT) € 7, Noms de domaine mylovelab.fr + myrelation.fr (≈ 19 €/an) € 2, Abonnement IA pour le développement et le contenu (Claude, estimation) € 90, Banque pro en ligne pour micro-entreprise (estimation) € 9, Salaires fondateurs € 0).

- **Break-even: 2 couple-mois (un mois de Duo payé par un couple, mix mensuel 9,90 € / annuel 59 €)s a day.** Below that you lose money every month.
- **Profit margin at your plan** (10 a day): **47%** of every sale, after every cost.

### Year 1, month by month

| month | couple-mois (un mois de Duo payé par un couple, mix mensuel 9,90 € / annuel 59 €)s a day | revenue | profit | cumulative (after € 2,040 startup) |
| ---: | ---: | ---: | ---: | ---: |
| 1 | 0 | € 78 | -€ 107 | -€ 2,147 |
| 2 | 1 | € 197 | -€ 44 | -€ 2,191 |
| 3 | 2 | € 474 | € 104 | -€ 2,087 |
| 4 | 3 | € 633 | € 189 | -€ 1,898 |
| 5 | 3 | € 751 | € 252 | -€ 1,646 |
| 6 | 4 | € 870 | € 316 | -€ 1,331 |
| 7 | 4 | € 988 | € 379 | -€ 952 |
| 8 | 5 | € 1,107 | € 442 | -€ 510 |
| 9 | 5 | € 1,263 | € 526 | € 16 |
| 10 | 6 | € 1,422 | € 610 | € 627 |
| 11 | 7 | € 1,581 | € 695 | € 1,322 |
| 12 | 7 | € 1,737 | € 779 | € 2,101 |

- **Year 1 operating profit: € 4,141** on € 11,101 of revenue.
- After the € 2,040 startup spend: € 2,101.
- Startup money earned back: month 9.
- Cash you need before it pays for itself: **€ 2,191**.

### What if

| scenario | margin at plan | break-even a day | year 1 profit |
| --- | ---: | ---: | ---: |
| Base plan | 47% | 2 | € 4,141 |
| Price -10% | 41% | 2 | € 3,031 |
| Volume -20% | 46% | 2 | € 2,955 |
| Unit costs +15% | 40% | 2 | € 3,365 |

No red flags in these numbers. They are only as good as the inputs: check every cost against a real quote.

## Marketing

Sources : `idea.md`, `site-notes.md`, `board.md`, `competitors.md`, `panel/results.md` (v2, 5 achats sur 30), `panel-v1/results.md` (0 sur 20), `offer.md`, `pricing.md`, `cfo.md`, `customer.json`. Les acheteuses du panel sont simulées : leurs mots guident les messages, jamais comme témoignages. Pas un conseil juridique.

### 1. Ce que l'évidence dit

- **Qui achète** : les « fans de rituels à deux » (4 sur 4, mince) et les jeunes mamans (3 sur 7). Raison n°1 : l'habitude (« ça ressemble à un jeu de cartes couple et pas à une thérapie », P005). Les « curieuses des tests » (0 sur 8) et le « moment de tension » (0 sur 4) font le test et ne paient pas.
- **Pourquoi on refuse** : 22 refus sur 25 dépendent du partenaire (« il va dire oui, oublier, et ce sera moi qui le relance », P001). Ce que les refus demandent : « qu'il fasse le test de son côté sans que j'insiste », et l'offre à 49 € passe.
- **Le marché** : aucun bilan + programme par dimensions en français sous 10 €/mois sans app ; reproches n°1 à 3 des concurrents : gratuit vide, résiliation piégeuse, contenu répétitif.
- **Vendu** : Le Duo, 9,90 €/mois ou 59 €/an pour deux ; essai 14 jours qui ne démarre que quand les deux ont fait le test ; question du soir par notification ou e-mail ; 30 jours remboursés ; Offre fondateurs 49 €/an pour 100 couples jusqu'au 31 décembre.

### 2. Positionnement

**A. Le rituel du soir (recommandée)**
Pour les couples qui ont déjà un petit rituel à deux (jeu de cartes, questions du soir) et qui veulent « un truc qui nous fait rire deux minutes avant de dormir », MyLoveLab est le test de couple gratuit en français qui devient une question du soir à deux, vos deux regards côte à côte, pour moins qu'un jeu de cartes par mois, contrairement à Paired, un flux de questions en app à 14,99 €/mois sans bilan par dimensions.

**B. Après le bébé**
Pour les jeunes mamans qui « ne se parlent plus que de couches et de biberons », MyLoveLab est le programme par dimensions fondé sur la recherche, deux minutes par soir, 49 €/an pour deux, contrairement à une thérapie de couple à 60–120 € la séance, non remboursée.

**C. Le partenaire d'abord**
Pour les couples dont l'un est curieux et l'autre pas, MyLoveLab est le test de couple de 15 minutes, gratuit et sans compte, que chacun fait de son côté pour comparer, contrairement aux quiz de magazines et au « test de l'oiseau » qui ne disent rien sur vous deux.

**Choix : A comme ligne de marque, C comme message au partenaire.** Évidence : les 5 achats viennent du rituel (raison « habitude » 4 fois sur 5), et deux des trois jeunes mamans qui achètent le disent avec les mêmes mots (« petit rituel du soir », « moins qu'un jeu de cartes », P005, P006). B reste le message des créatrices parentalité. Le « moment de tension » amène des tests, pas des paiements (0 sur 4) : SEO, pas marque. C répond à l'objection n°1 : parler à l'homme autant qu'à l'acheteuse.

### 3. Canaux

| Canal | Pourquoi ce buyer | Coût | Ça a marché si |
|---|---|---|---|
| **SEO « test de couple », 17 articles, pages par paires de profils** | Lectrice psycho et moment de tension cherchent sur Google le soir ; aucun concurrent n'est web-first | 0 €, temps de Laurène | Tests terminés depuis Google en hausse chaque semaine (GA4), complétion ≥ 50 % |
| **Créatrices psy affiliées** (Instagram/TikTok, 30 % sur 12 mois, sans fixe, lien `?ref=` et code Stripe) | « Tu as déjà envoyé un reel de psy à ton partenaire » | 0 € fixe ; contribution ramenée à 3,17 € sur ces couples | 10 créatrices signées (objectif fondateurs), tests par `?ref=`, invitations ≥ 30 % |
| **Praticiens partenaires** (30 % + Duo offert, page praticiens visible) | Caution face à « c'est quoi cette marque » | 0 € fixe | 20 actifs (objectif) ; codes utilisés ; pas une source de volume |
| **La boucle d'invitation** (lien « fais le test de ton côté », lettre au partenaire v3) | 22 refus sur 25 : chaque test terminé est une impression gratuite chez l'autre | 0 € | Invitations ≥ 30 % des tests terminés, invités qui terminent ≥ 50 % |
| **Pinterest et Google « jeu couple »** (pages des 6 jeux, épingles « questions couple ») | Le segment qui paie cherche des jeux à deux, pas de la thérapie | 0 €, 1 h/semaine | Tests arrivant par les pages jeux |
| **« Offrir le Duo » à Noël** : l'Offre fondateurs à 49 € par lien Stripe + PDF, zéro développement | La femme achète ; un cadeau fait entrer le partenaire sans « on a un problème » | 50 € de boost | Duo offerts du 14 au 23 décembre |
| **Meta ads, retargeting seulement** (test terminé sans invitation ou sans paiement) | Audience chaude ; 0,90 € par test est irréaliste à froid | 150 € en décembre, pixel à poser avant | ≤ 30 € par couple payant, visé 10 € |

**On commence avec trois** : créatrices psy (Jules), SEO + boucle d'invitation (Laurène), retargeting à 150 € (pour mesurer).

**Ce qu'on ne fait pas** : DM, mails froids et groupes Facebook (4 réponses sur 160, « peu marché ») ; TikTok ads à l'échelle (pas de pixel, pas de créa testée, cap de 0,90 € par test) ; appli native (hors de portée à 15 h/semaine ; PWA + e-mail du soir) ; remise Saint-Valentin (`pricing.md` : carte cadeau au prix normal, 59 €).

**Règles** : tout post de créatrice ou de praticien rémunéré porte « Collaboration commerciale » / #collaboration dès le début (loi du 9 juin 2023 sur l'influence commerciale, à faire relire). Jamais « diagnostic », « thérapie », « sauver son couple » : « sessions ludiques », « ne remplace pas un thérapeute », violences → 3919. Pas de faux avis, pas de « vu sur », pas de chiffres de followers.

### 4. Les 30 jours

Instagram : 2 posts/semaine (mardi, vendredi) ; le reste en stories, e-mails, partenaires. Prérequis avant le 7 décembre : entité juridique, Stripe, pixel Meta, e-mail du soir, « Vos deux regards » validé par 10 couples bêta (`board.md`).

| Date | Canal | Message |
|---|---|---|
| Lun 23 nov (J−14) | Créatrices (Jules) | 10 premiers mails aux psy-créatrices : test à faire elles-mêmes, lien `?ref=`, 30 %/12 mois |
| Mar 24 | Instagram | Accroche 4 : « Vous avez un jeu de cartes couple qui traîne ? » |
| Mer 25 | Technique | Pixel Meta, événements GA4 « test terminé », « invitation », « paiement » |
| Jeu 26 | E-mail bêta | Offre fondateurs 49 €/an ouvre le 7/12, 100 places |
| Ven 27 | Instagram | Accroche 9 : « Le test est complet et gratuit » |
| Sam 28 | Stories | Making-of : Laurène écrit une session, montre l'étude citée |
| Dim 29 | Pinterest | 10 épingles « questions couple du soir » vers les pages jeux |
| Lun 30 (J−7) | Praticiens | Relance des 4 positifs : code personnel, Duo offert, page praticiens |
| Mar 1 déc | Instagram | Accroche 1 (au partenaire) : « 15 minutes, pas de compte » |
| Mer 2 | Blog | « 30 questions couple pour ce soir » (requêtes « jeu couple ») |
| Jeu 3 | Stories | « Vos deux regards » du couple fondateur |
| Ven 4 | Instagram | Accroche 8 : « L'essai ne commence que quand vous êtes deux » |
| Sam 5 | Créatrices | Kit : 3 scripts dont 2 au partenaire, mention « Collaboration commerciale » |
| Dim 6 | E-mail | Testeuses sans invitation : « ton partenaire n'a pas fait le test ? voilà le lien court » |
| **Lun 7 déc (J0)** | Tous | Lancement payant : Offre fondateurs, places restantes réelles ; post, stories, e-mail |
| Mar 8 | Instagram | Accroche 10 : « 100 couples, 49 € l'année pour deux, jusqu'au 31 décembre » |
| Mer 9 | Meta retargeting | Test terminé sans invitation, accroches 1 et 2, 10 €/jour |
| Jeu 10 | Stories | Chiffre réel de la semaine (tests terminés) |
| Ven 11 | Instagram | Accroche 3 : « 5 questions où les couples ne répondent pas pareil » |
| Sam 12 | Créatrices | Premières publications affiliées, repartage en story |
| Dim 13 | E-mail | Testeuses sans paiement : 30 jours remboursés, résiliation en un clic |
| Lun 14 (J+7) | « Offrir le Duo » | Lien Stripe + PDF cadeau ; stories « le cadeau qui n'est pas un reproche » |
| Mar 15 | Instagram | Accroche 6 : « Depuis le bébé, vous ne parlez que logistique ? » |
| Mer 16 | Meta boost | 50 € sur le post cadeau, audiences chaudes, jusqu'au 20 |
| Jeu 17 | Praticiens | Deuxième vague : 20 praticiens, page et premiers chiffres réels |
| Ven 18 | Instagram | Accroche 5 : « 9,90 € pour deux, résiliable en un clic » |
| Sam 19 | Stories | Jeu « Tu préfères » en sondage, 3 cartes |
| Dim 20 | E-mail | Dernier rappel cadeau avant Noël |
| Lun 21 (J+14) | Bilan | Les trois chiffres ; on garde ou on coupe le retargeting |
| Mar 22 | Instagram | Accroche 7 : « On ne vous demande pas de nous croire » |
| Mer 23 (J+16) | Stories + e-mail | « Il reste N places fondateurs, fin le 31 décembre » (N réel) |

Fin de l'Offre fondateurs : 31 décembre 2026, puis 59 €/an. Pas de compte à rebours artificiel.

#### Les dix accroches

1. **Vidéo, 3 s, au partenaire** : « 15 minutes, pas de compte, et tu vois si vous voyez la même chose. » (« il ne fera jamais ça »)
2. **Titre de pub, au partenaire** : « Elle a fait le test. À toi : 15 min, sans inscription, pour comparer. » (« qu'il fasse le test de son côté »)
3. **Carrousel, au partenaire** : « 5 questions du test où les couples ne répondent pas pareil (et pourquoi c'est normal) » (« pas un interrogatoire de psy »)
4. **Vidéo, 3 s** : « Vous avez un jeu de cartes couple qui traîne ? Voilà la version du soir, en deux minutes. » (raison d'achat : le rituel)
5. **Titre de pub** : « 9,90 € par mois pour deux. Résiliable en un clic, sans question. » (« le prix de Netflix », « encore un abonnement à résilier »)
6. **Carrousel** : « Depuis le bébé, vous ne parlez que couches et biberons ? Une question par soir, 7 dimensions. » (raison d'achat, P019)
7. **Vidéo, 3 s** : « On ne vous demande pas de nous croire : chaque session cite son étude. » (« c'est quoi cette marque », « test de magazine »)
8. **Titre de pub** : « L'essai ne commence que quand vous êtes deux. » (« je paie pour un partenaire absent »)
9. **Carrousel** : « Le test est complet et gratuit. Voilà tout ce que vous voyez sans payer. » (reproche n°1 du marché)
10. **Vidéo, 3 s** : « 100 couples, 49 € l'année pour deux, jusqu'au 31 décembre. Après, c'est 59. » (« je ne m'abonne jamais derrière un test »)

Réserve, charge mentale : « Une question le soir ne fera pas la vaisselle. Mais elle dit qui pense aux courses. » (P021)

#### Quand il n'y a rien de neuf
Le making-of (Laurène écrit une session et montre la source), une carte de jeu en sondage, le chiffre réel de la semaine, l'histoire de Laurène et Jules (sept ans, à distance, page À propos), une réponse à une question reçue. Jamais un témoignage qu'on n'a pas, jamais un avant/après.

### 5. Budget et chiffres

**Le maximum par couple payant** : 4,22 € de contribution × 7 mois de rétention moyenne (churn 15 %) = **29,54 € ≈ 30 €** ; le panel achète 1,0 fois par mois, rien à multiplier. Visé : 10 €. À 3 % de paiement : au plus 0,90 € par test terminé, 0,30 € visé. Un couple venu par une créatrice vaut ≈ 22 € (3,17 € × 7) : jamais commission et pub sur le même couple.

**150 € (Noël, 9–23 décembre)** : 100 € de retargeting Meta sur les testeuses sans invitation ou sans paiement (accroches 1, 2, 8), 50 € de boost du post « Offrir le Duo ». Rôle : un premier coût réel, pas du volume. Garde-fou : après 50 € dépensés, si le coût par test terminé dépasse 0,90 €, on coupe.

**600 € (janvier)** : 350 € de retargeting, 150 € de boost des deux meilleures vidéos de créatrices (« Collaboration commerciale », avec leur accord), 100 € d'essai Google Search sur « test de couple » en mot-clé exact. Seuil (`cfo.md`) : au moins 20 couples payants pour ne pas perdre la mise, 60 pour être au but, soit ≥ 667 tests terminés à 0,90 €.

**1 000 € (Saint-Valentin)** : versés seulement si janvier sort sous 30 € par couple. 600 € de boost des contenus de créatrices, 300 € de retargeting, 100 € Pinterest/Google « cadeau couple » vers la carte cadeau Duo à 59 €. Sinon, les 1 000 € restent en caisse.

**Les trois chiffres de la semaine**

| Chiffre | Objectif | On change quelque chose si |
|---|---|---|
| Tests terminés (complétion ≥ 50 %) | ≈ 80/semaine en décembre (10 couples fondateurs ÷ 3 % ≈ 333 tests sur le mois) ; 160–300/semaine au printemps (`cfo.md`) | < 40/semaine deux semaines de suite : revoir le kit créatrices et le SEO ; complétion < 50 % : raccourcir le test |
| Invitations du partenaire | ≥ 30 % des tests terminés ; ≥ 50 % des invités terminent | < 20 % deux semaines : réécrire la lettre au partenaire, accroches 1–3 en premier ; invités qui ne finissent pas : revoir leur page d'arrivée |
| Paiement | ≥ 3 % des tests terminés ; ≤ 30 € par couple | < 1,5 % après 200 tests : couper la pub, retour à `offer.md` ; essais à deux qui ne convertissent pas : revoir les 14 jours |

**Non sourcé** : les coûts par clic ou par mille en France (le budget de Noël sert à les mesurer), le nombre actuel de tests et d'abonnés Instagram (jamais cités ici), l'audience des créatrices (à demander avant signature). La carte cadeau n'est pas dans `offer.md` : ramenée à un lien de paiement sans développement, conformément au gel des briques du board.

Suite : `/founder-brand`, puis `/founder-launch`.

## Brand

Brief suivi (positionnement du marketing) : pour les couples installés depuis 2 à 7 ans qui ne se parlent plus que logistique, le test de couple gratuit, fondé sur la recherche, qui montre vos deux regards, puis le Duo : une question du soir à deux, deux minutes, 9,90 € pour vous deux ; contrairement à Paired et aux quiz de magazine. Sources : `idea.md`, `site-notes.md`, `board.md`, `competitors.md`, `panel/results.md`, `offer.md`, `pricing.md`, `pitch.md`.

Le nom est choisi et en usage : **MyLoveLab** (ex-MyRelation, mylovelab.fr, logo cœur-flèche, rose #FC355A, Instagram). Ce document ne le remet pas en cause. Ce que la marque doit tenir, d'après le panel (« ça ressemble à un jeu de cartes, pas à une thérapie ») : un jeu que l'on sort le soir, sourcé comme un bon livre, jamais un cabinet. L'objet que l'on partage, « Vos deux regards », porte la marque plus que le logo.

### 1. Les vérifications sur le nom existant

Recherches publiques seulement ; un conseil en propriété industrielle confirme, et rien n'est protégé tant que rien n'est déposé. Pas un avis juridique.

**Marque.** Chercher « mylovelab », « my love lab », « love lab », « lovelab » sur la base INPI (https://data.inpi.fr/, Marques) et sur TMview (https://www.tmdn.org/tmview/), qui couvre les marques de l'Union européenne valables en France. Classes : **9** (logiciels, applications), **41** (éducation, divertissement : les sessions ludiques), **42** (SaaS), **44** (santé, conseil psychologique : là où vos pages « thérapie de couple » peuvent vous ranger). Deux faits connus : le **Love Lab** est le laboratoire historique du Gottman Institute (gottman.com/professionals/love-lab), que MyLoveLab cite comme source, ce qui rend le rapprochement visible ; et **mylovelab.ca** appartient à une coach de couple canadienne. Lecture : un nom fait de mots courants est faiblement distinctif, donc difficile à défendre, mais peu susceptible d'être bloqué en France sans dépôt antérieur. Le vrai risque est la confusion : « love lab » sur Google mène à Gottman, et le Québec bute sur le .ca. À faire avant d'encaisser : la recherche, puis un dépôt en 9, 41, 42 (44 avec le conseil). Ne jamais écrire « le Love Lab » seul : toujours **MyLoveLab**, un mot, trois majuscules.

**Domaines.** mylovelab.fr est à vous. Vérifier, pas supposer : **mylovelab.com**, **.app**, **.co**, .eu, my-love-lab.fr, lovelab.fr. Prendre le .com s'il est libre ; sinon rester sur le .fr, et garder myrelation.fr en redirection 301 au moins douze mois.

**Handles.** Vérifier @mylovelab sur Instagram (lequel est le vôtre exactement ?), TikTok, YouTube, X, Pinterest ; repli uniforme **@mylovelab.fr** partout.

**Confusion.** LovBirdz (Nantes, français) et Love Nudge partagent le mot « love » ; Lasting et Paired, rien. Le suffixe « Lab » vous distingue. Règle : la marque va toujours avec son descripteur, « MyLoveLab, le test de couple », jamais seule dans un titre.

### 2. Nommer l'offre et le produit (cinq noms)

| Nom | À l'oral | Dans une notification | Risque |
|---|---|---|---|
| **Le Duo** (le produit payant : un produit, pour deux, un paiement) | deux syllabes, « on a pris le Duo » | « Le Duo · ta question du soir » | générique : toujours « le Duo MyLoveLab » |
| **Ton regard / Vos deux regards** (résultat solo, puis carte à deux ; aucun verdict) | doux, s'entend comme une phrase | « Vos deux regards sont prêts » | « regard » peut sonner jugement : jamais à côté d'un score global |
| **La question du soir** (le rituel : une question, un moment, pas un programme) | plat et rassurant, comme « la météo du soir » | la notification porte la question elle-même | descriptif donc copiable ; c'est voulu |
| **Les 14 soirs** (l'essai, qui ne démarre que quand vous êtes deux) | plus concret que « 14 jours d'essai » | « Soir 3 sur 14 : ce soir, à deux » | un compteur culpabilise : ne jamais afficher les soirs manqués |
| **Offre fondateurs**, badge « 100 couples fondateurs » (le lancement) | solennel sans être pompeux | « Il reste 37 places fondateurs » (si c'est vrai) | un compteur faux détruit la marque |

Pas de « Premium », d'« Essentiel » ni de « Pro » : *ton regard, vos deux regards, la question du soir, 14 soirs, le Duo.*

### 3. La voix et la promesse

**Règle d'adresse.** « Tu » à la personne qui lit, « vous » pour le couple, jamais le vous de politesse. Inclusif par construction : « ton ou ta partenaire », ou mieux, le prénom.

**La promesse.** « Deux minutes par soir, à deux, et vous vous comprenez un peu mieux. » Elle garde la promesse publique actuelle (« Mieux vous comprendre à deux, en quelques minutes par jour ») en la rendant tenable : deux minutes, un soir, un peu mieux. Pas « sauver ».

**Trois taglines.**
1. **« Vos deux regards sur votre couple. »** Recommandée : elle nomme l'objet que l'on partage, tient en bio Instagram, et aucun concurrent ne parle de regards.
2. « Deux minutes le soir, à deux. » Pour le Duo et les pubs.
3. « Se parler d'autre chose que des courses. » Pour les reels et les créatrices : l'insight du brief, avec un sourire.

Le titre actuel, « le test qui révèle où en est ton couple », sonne comme un verdict. Proposition : **« Le test gratuit qui montre comment tu vois ton couple. »**

**La voix en trois adjectifs.**
- **Chaleureuse.** Fais : parle du soir, du canapé, du prénom (« ce soir, avec Léa »). Ne fais pas : « votre relation présente des points d'amélioration », ni les points d'exclamation en rafale.
- **Franche.** Fais : cite la source en une ligne (« d'après les travaux de Gottman ») et dis ce que le test ne fait pas (« ne remplace pas un ou une thérapeute »). Ne fais pas : « scientifiquement prouvé », « 89 % de couples transformés », « diagnostic ».
- **Ludique.** Fais : « sessions ludiques », « jeu », « question », « deux minutes ». Ne fais pas : « programme d'amélioration », « séance », « thérapie », « profil », « sauver son couple ». Jamais d'étiquette figée : pas « tu es Protecteur » mais « aujourd'hui, tu te reconnais dans le portrait Protecteur ».

**Avant / après (une ligne de `pitch.md`).**
Avant : « Chaque soir, une question ou une session ludique de 5 à 8 minutes, à faire à deux en deux minutes depuis la notification, ou plus longuement quand vous avez le temps. Si vous ratez des jours, rien ne se perd. »
Après : « Chaque soir, une question pour vous deux. Deux minutes depuis la notification, plus si vous avez envie de creuser. Un soir raté ? Rien ne se perd. »

Le cadre de sécurité, même voix : « MyLoveLab ne remplace pas un ou une thérapeute. Si ça dépasse une question du soir, on te montre vers qui te tourner. En cas de violence : le 3919, gratuit et anonyme. »

### 4. Le look, en brief

**Couleurs.** Tout part du rose existant, mais il ne peut pas tout faire.
- **Rose MyLoveLab #FC355A** : l'accent. Logo, bouton principal, cœur, progression, le « toi » sur la carte. Contraste mesuré : **3,62:1** sur blanc, et **3,62:1** pour du texte blanc posé dessus. Sous le seuil AA du texte courant (4,5:1) ; suffisant pour les gros titres (≥ 24 px, ou 19 px gras) et les composants d'interface (3:1). Donc pas de paragraphe ni de lien en rose, et un bouton rose à texte blanc porte un libellé gras d'au moins 19 px. Pour du rose lisible, **#C8143A** (5,81:1 sur blanc).
- **Encre nuit #1F1A2E** : le texte. 16,86:1 sur blanc, 15,64:1 sur lin ; un violet très sombre, plus doux qu'un noir. Aussi fond des cartes « nuit » (rose dessus : 4,65:1, conforme).
- **Lin #FFF4F2** : le fond des pages, cartes et e-mails, pour que le blanc pur ne fasse pas « formulaire médical ».
- **Sauge profonde #1E6B5C** (troisième couleur, usage précis) : le « lui ou elle » sur la carte et les états « c'est fait ». 6,34:1 sur blanc, blanc dessus 6,34:1. Pas genrée : jamais rose contre bleu pour deux partenaires.

**Typo (Google Fonts, licence SIL OFL, gratuites).** Display : **Fraunces** (https://fonts.google.com/specimen/Fraunces), serif chaleureuse, pour les titres, la question du soir et les prénoms sur la carte ; elle dit « livre que l'on aime », pas « appli de santé ». Texte : **Figtree** (https://fonts.google.com/specimen/Figtree), sans-serif ronde, nette en petit, pour l'interface, les scores et les e-mails ; corps 17 px minimum sur mobile. Aucune autre police sans licence.

**Brief logo (le cœur-flèche existant).** Ce qu'il doit dire : deux regards qui se rejoignent, léger, pas blessé. Où il doit marcher, à tester un par un : **favicon 32 px** (et 16 px : flèche visible, trait épais), **icône PWA** sur l'écran d'accueil (« maskable » : symbole dans les 80 % centraux, fond rose, cœur blanc), **avatar Instagram** (cercle : rien dans les coins), **en-tête d'e-mail** (lockup horizontal, 40 px de haut), **la carte « Vos deux regards » en story** (monochrome, petit, en bas). Donc quatre fichiers : symbole seul, lockup, blanc, encre. À éviter : dégradés et relief, Cupidon, cœur brisé ou recousu, silhouettes homme-femme, deux moitiés rose et bleu, et surtout pas d'éprouvette pour illustrer « Lab » (le clinique que la voix interdit). Rien qui ressemble à un concurrent de `competitors.md` ; un concept généré par un outil d'image reste un concept.

**Les cinq premiers points de contact.**
1. **Le hero de l'accueil.** Titre : « Le test gratuit qui montre comment tu vois ton couple. » Sous-titre : « 15 minutes, sans inscription, fondé sur 50 ans de recherche. Envoie le lien, et vous découvrez vos deux regards côte à côte. » Bouton rose : « Faire le test ». En petit : « Gratuit, anonyme. Ne remplace pas un ou une thérapeute. » Visuel : la carte, pas une photo de couple.
2. **La carte « Vos deux regards »** (ce que les gens postent ; 1080×1920 et 1080×1080). Fond lin, deux prénoms en Fraunces, sept dimensions en deux barres côte à côte (rose pour l'un, sauge pour l'autre), une phrase en haut : « On voit pareil sur 5 dimensions sur 7 », une en bas : « Là où nos regards diffèrent le plus : le projet commun ». Pas de score global ni de « compatibilité à 72 % » (le panel : « pas juste des pourcentages »), rien sur l'autre sans son accord. Logo en bas, « mylovelab.fr ».
3. **Le message d'invitation du partenaire** (pré-écrit, modifiable, l'objection n° 1 du panel) : « J'ai fait un test de couple, 15 min, gratuit, sans compte, et j'ai mes résultats. Curieux·se de voir si tu vois les choses pareil ? Fais-le de ton côté et on compare : [lien] ». Jamais « on a un problème », jamais « il faut qu'on parle ».
4. **La notification du soir.** Titre : « MyLoveLab ». Corps : la question, 90 caractères maximum, jamais rien d'intime ni un résultat (écran verrouillé) : « Ce soir, à deux : le moment de la semaine où tu t'es senti·e le plus proche de Léa ? » Une par jour, à l'heure choisie par le couple, arrêt après sept soirs sans ouverture, jamais de relance culpabilisante (« la question d'hier t'attend » oui, « tu nous as manqué » non).
5. **La réponse à la première réclamation**, « je n'arrive pas à résilier » : « Bonjour Camille, c'est fait : ton Duo est résilié, tu gardes l'accès jusqu'au [date] et rien ne sera prélevé. Désolée que le bouton ait été dur à trouver (Compte, Abonnement) : je le rends plus visible cette semaine. Si tu veux le remboursement des 30 derniers jours, dis-le-moi, je le fais sans question. Laurène. » Le prénom, le fait accompli, jamais « votre demande a été prise en compte ».

### 5. À signaler

- #FC355A ne passe pas en texte courant ni sur un bouton à petit libellé : encre pour le texte, #C8143A pour les liens.
- « Love Lab » (Gottman) et mylovelab.ca existent : recherche INPI/TMview et dépôt avant le 7 décembre, avec un conseil.
- Le site dit « session courte » plusieurs fois (règle : « session ludique ») et « révèle où en est ton couple » : à réécrire ; et pour les 24 portraits, toujours « tu te reconnais dans », jamais « tu es ».

Suite : `/founder-ops` et `/founder-launch`.

## Operations

Méthode `founder-ops` adaptée à un abonnement en ligne : pas de marchandises, pas de local. Sources : `idea.md`, `offer.md`, `pricing.md`, `numbers.json`, `cfo.md`, `site-notes.md`, `/tracking/`. Prix publics relevés le 19/11/2026, à revérifier au moment de payer ; estimations marquées. **Pas un conseil juridique, comptable ou fiscal.**

### 1. Le cycle quotidien et hebdomadaire

Ce que voit le couple est marqué **[client]**.

**Automatique**
- **[client]** Test gratuit sans compte → compte → code d'invitation → le partenaire fait le test de son côté → « Vos deux regards » → l'essai Stripe de 14 jours démarre à cet instant (brique 1).
- **[client]** 20 h 30 : web push avec la question du soir (PWA, brique 2) ; sans push délivré sous 10 min, e-mail de secours (brique 3). J-3 avant la fin de l'essai : e-mail « 9,90 €/mois ou 59 €/an, résiliable en un clic ».
- Stripe : encaissement, relances d'impayé, factures, coupure de l'accès par webhook. Supabase : sauvegarde quotidienne, table `stripe_events`. Clarity et GA4 (version consentement de `head-tracking.html`) : événements `test_termine`, `invitation_acceptee`, `essai_demarre`, `paiement`.

**Chaque jour** : routine 1 (15 min, Laurène ; Jules en secours) ; **[client]** réponse à `contact@mylovelab.fr` sous 24 h, 48 h le week-end.

**Chaque semaine** : lundi, tableau de bord (Jules : tests terminés, invitations, essais, paiements, churn, remboursements, face aux KPI ≥ 50 % / ≥ 30 % / ≥ 3 %) ; mardi, correctifs et déploiement (Laurène) ; vendredi, commissions (routine 5) ; week-end, contenu/SEO (routine 6) ; dimanche soir, 30 min à deux sur les risques.

### 2. « Fournisseurs » : outils et services

| service | rôle | prix public | source |
|---|---|---|---|
| Vercel Pro | hébergement commercial (Hobby interdit) | 20 €/mois par membre ≈ 18,50 € | [vercel.com/pricing](https://vercel.com/pricing) |
| Supabase Pro | base, auth, sauvegardes 7 j, pas de pause | 25 €/mois ≈ 23 € | [supabase.com/pricing](https://supabase.com/pricing) |
| Stripe | abonnements, essai, remboursements, codes promo | 1,5 % + 0,25 € carte UE ; 2,5 % UK ; 3,25 % hors UE | [stripe.com/fr/pricing](https://stripe.com/fr/pricing) |
| Brevo (ou Resend) | rappels et transactionnels | gratuit ≤ 300 e-mails/jour, Starter ≈ 7 € HT/mois ; Resend gratuit 3 000/mois, Pro 20 € | [brevo.com](https://www.brevo.com/fr/pricing/), [resend.com](https://resend.com/pricing) |
| Web push | question du soir | service worker + VAPID : 0 € ; ou OneSignal gratuit (≤ 10 000 abonnés web par envoi), Growth dès 19 €/mois | [onesignal.com/pricing](https://onesignal.com/pricing) |
| Clarity, GA4 | mesure, enregistrements | gratuits | [clarity.microsoft.com](https://clarity.microsoft.com) |
| Canva | visuels | gratuit ; Pro ≈ 110–120 €/an (sources tierces) | [canva.com/fr_fr/tarifs](https://www.canva.com/fr_fr/tarifs/) |
| OVHcloud | mylovelab.fr + myrelation.fr | .fr ≈ 7,79 € HT/an, ≈ 19 € TTC pour deux | [ovhcloud.com](https://www.ovhcloud.com/fr/domains/tld/fr/) |
| Shine | compte dédié | gratuit ; Start ≈ 9 € HT/mois | [shine.fr/tarifs](https://shine.fr/tarifs) |
| Affiliation | suivi des commissions | **A** : codes promo Stripe + cookie `?ref=` en base, 0 € ; **B** : Rewardful dès 49 €/mois, Tolt dès 69 €/mois | [rewardful.com](https://www.rewardful.com/pricing), [tolt.io](https://tolt.io/pricing) |

**Écarts avec `numbers.json` (le CFO doit relancer ; fichier non modifié)**
1. **Cotisations micro : 25,6 % en 2026 pour le BNC**, pas 24,6 % (taux 2025) ; 21,2 % si l'activité est classée BIC. L'**ACRE** tombe de 50 % à 25 % d'exonération au 1er juillet 2026 et n'est plus automatique ([economie.gouv.fr](https://www.economie.gouv.fr/entreprises/micro-entreprise-auto-entreprise-charges-sociales)). Impact : +0,08 €/couple-mois (BNC) ou −0,27 € (BIC) ; à trancher avec l'URSSAF.
2. **E-mailing : 0 € au lancement** (300/jour couvrent ≈ 120 couples), puis ≈ 7 € HT au lieu de 9 € ; domaines ≈ 1,60 €/mois au lieu de 2 € ; INPI 230 € si deux classes (41 et 44).
3. Options non chiffrées : RC pro ≈ 13 €/mois ; outil d'affiliation 49 €/mois seulement au-delà de ~30 affiliées.

### 3. Les gens

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

### 4. Les routines (SOP)

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

### 5. La pile minimale

Vercel Pro 18,50 € + Supabase Pro 23 € + Brevo 0 puis 7 € + push maison 0 € + Clarity, GA4, Canva 0 € + domaines 1,60 € + Shine 0 (ou 9 €) + IA 90 € (estimation ; 20 € si Claude Pro suffit) = **133 à 160 €/mois**, cohérent avec les 149 € de `numbers.json`. Stripe en variable ; affiliation option A à 0 €. Comptabilité : tableur et déclaration URSSAF mensuelle ; comptable (≈ 50 €/mois) seulement en société.

### 6. Checklist légale et administrative (France)

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

### 7. Registre des risques

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

## Launch plan

Méthode : `founder-launch`. Colonne vertébrale : la checklist de `board.md`. Sources : `offer.md`, `pricing.md`, `cfo.md`, `panel/results.md` (v2 : 5 achats sur 30), `panel-v1/results.md` (0 sur 20). Le calendrier marketing vit dans `marketing.md`, la checklist légale et le registre des risques dans `ops.md`, la carte de résultat et les textes de notification dans `brand.md` : ce plan les appelle sans les réécrire.

Aujourd'hui : jeudi 19 novembre 2026. Sortie payante visée : **lundi 7 décembre 2026**. Repli : **lundi 14 décembre**. Laurène a 15 h par semaine (soirs ~1 h 30, mardi 3 h, samedi et dimanche 3 h chacun) ; Jules prend tout ce qui n'est pas du code.

### 1. Le test réel avant de dépenser

#### Test A : la pré-vente fondateurs

Pour un abonnement, le test le moins cher est l'offre fondateurs payée d'avance : **49 €/an pour le couple, 100 places, jusqu'au 31 décembre, encaissé via un lien de paiement Stripe**. Pas de liste d'attente : une carte bancaire.

**Ligne de succès, écrite avant de lancer : 10 couples payants parmi les 50 couples bêta avant le lundi 7 décembre** (objectif des fondateurs, repris dans `pricing.md`). Le lien n'existe qu'une fois l'entité créée et Stripe en mode réel (section 2) ; s'il n'est pas en ligne le lundi 30 novembre, la ligne est mesurée 7 jours après sa mise en ligne, au plus tard le 14 décembre.

**Règle de comparaison avec le panel.** Le panel v2 achète à 17 % ; 10 sur 50 ferait 20 %.
- **10 ou plus** : le réel confirme le panel ; on lance, les 600 € de janvier restent en jeu (décision le 6 janvier).
- **5 à 9** : on lance, mais les 600 € sont gelés tant que le canal qui a amené ces couples n'a pas un coût connu.
- **Moins de 5** : les vrais acheteurs disent non là où le panel disait oui ; on les croit. Retour à `/founder-offer` (mode solo, lettre au partenaire) ou à `/founder-pricing` **avant** le premier euro des 600 €. Le 7 décembre reste (il ne coûte rien), la pub non.

Jules note le profil de chaque couple payant (le panel dit couples « à rituel » et jeunes mamans) pour que `marketing.md` cible juste.

#### Test B : le blocage n° 1 du panel

22 refus sur 25 tiennent à « mon partenaire ne le fera jamais ». Seuls de vrais couples tranchent. Sur les 50 couples bêta, dès le 30 novembre :
- **acceptation de l'invitation partenaire : objectif ≥ 30 %** (KPI des fondateurs). En dessous, mode solo et lettre au partenaire passent devant toute brique de janvier ;
- **retour à J1 et J7** après le premier soir à deux. Le board exige un objectif J7 fixé avant le 7 décembre ; les fondateurs ne l'ont pas écrit. Proposition à valider : 50 % des couples en essai reviennent au septième soir, la barre de la complétion du test.

Ces chiffres sont la première condition du board : Laurène les sort de Clarity et Supabase cette semaine.

### 2. Le compte à rebours

**[CC]** = chemin critique, une glissade décale la sortie. L = Laurène, J = Jules.

#### Semaine 1 : jeudi 19 → dimanche 22 novembre

| quoi | qui | échéance |
|---|---|---|
| **[CC] Déclarer la micro-entreprise** (guichet unique), pièces selon `ops.md` | J | ven. 20 nov. |
| Chiffres réels du site (Clarity, Supabase), 1 h | L | ven. 20 nov. |
| **[CC] Migration de domaine** préparée : redirections app.myrelation.fr → mylovelab.fr, liens des e-mails et de /duo (soirs jeu., ven.) | L | ven. 20 nov. |
| **Brique 1, Stripe et offre fondateurs** en mode test : Duo 9,90 €/mois et 59 €/an, fondateurs 49 €/an limité à 100, essai 14 jours qui ne démarre que quand les deux ont fait le test, résiliation en un clic (week-end, 6 h) | L | dim. 22 nov. |
| Liste nominative des 50 couples bêta (réseaux des deux écoles, abonnés Instagram, couples « à rituel ») ; relance des 4 praticiens positifs : page partenaire, code ?ref=, Duo offert, « envoyez-nous 2 couples » | J | dim. 22 nov. |

#### Semaine 2 : lundi 23 → dimanche 29 novembre

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

#### Semaine 3 : lundi 30 novembre → dimanche 6 décembre

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

#### Du 7 au 31 décembre

Revues J7 (lun. 14 déc.) et J14 (lun. 21 déc.), section 4. Les 150 € de Noël ne partent pas avant le 14 décembre, après 10 couples passés par les coutures (board : aucun euro de pub avant), chaque euro étiqueté par canal, dates dans `marketing.md` (J). Jeudi 31 décembre à minuit : fin de l'offre fondateurs, passage à 59 €/an, compte des places vendues (L). Tout décembre : corrections de bugs seulement (section 5).

### 3. Le jour J : lundi 7 décembre 2026

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

### 4. Les 30 premiers jours

#### Les chiffres de la semaine (Jules, chaque lundi)

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

#### Les trois revues

**J7, lundi 14 décembre.** Combien de couples payants, dans quel groupe ? Invitation au-dessus de 30 % ? Retour le lendemain du premier soir ? Les 150 € de Noël partent-ils, sur quel canal ? Qu'est-ce qui a cassé le jour J ? Si no-go le 4, cette date devient le jour J et la revue glisse au 21.

**J14, lundi 21 décembre.** Les premiers essais arrivent à échéance : combien convertissent, combien annulent, pourquoi ? Le rappel J−3 est-il parti ? Un canal a-t-il un coût par couple connu et inférieur à 30 € ? Les 4 praticiens ont-ils envoyé un couple chacun ?

**J30, mercredi 6 janvier 2027 : la décision sur les 600 € de janvier.** On dépense si, et seulement si : (1) au moins 10 couples payants fondateurs au 31 décembre ; (2) invitation ≥ 30 % et J7 au-dessus de l'objectif fixé ; (3) remboursements ≤ 15 % ; (4) un canal mesuré sur les 150 € de Noël à moins de 30 € par couple, car les 600 € doivent produire au moins 20 couples payants pour ne pas être perdus (`cfo.md`). Sinon on garde l'argent, on retourne à `/founder-offer` ou `/founder-pricing`, et les 1 000 € de la Saint-Valentin se décident le lundi 8 février sur les mêmes critères. Même jour : la boucle a-t-elle été mesurée sur 50 couples ? Sinon le gel de la section 5 tient.

### 5. Ce qui est gelé

Jusqu'à ce que la boucle **test → Duo → retour le lendemain** soit mesurée sur 50 couples (invitation, essai, J1, J7, paiement), conformément au board, rien de ceci n'est codé ni annoncé : le jeu de cartes-questions, le calendrier des dates, les podcasts, la version anglaise, la carte cadeau Duo (pour la Saint-Valentin seulement si le gel est levé le 6 janvier), les sons, le pack « une dimension » à 14,90 €.

Seules briques autorisées en janvier : celles que les chiffres réclament, le web push si J7 est sous l'objectif, le mode solo et la lettre au partenaire si l'invitation est sous 30 %. Une seule à la fois.

Prochaine étape : `/founder-plan` compile le tout dans le plan d'affaires.

_The panel is simulated buyers and the numbers are projections from your inputs. Confirm demand with real customers and costs with real quotes before you spend. Not financial, legal or tax advice._
