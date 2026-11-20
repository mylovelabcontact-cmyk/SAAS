# Résumé

**MyLoveLab** (mylovelab.fr) est un site français pour les couples : un test de couple gratuit de 15 minutes, fondé sur la recherche, puis « le Duo », une question ou une session ludique chaque soir, à deux, pour 9,90 € par mois pour le couple ou 59 € par an. Il s'adresse d'abord aux femmes de 25 à 35 ans qui vivent avec leur partenaire depuis 2 à 7 ans, en France. Deux cofondateurs étudiants, Laurène et Jules, non rémunérés, 15 heures par semaine de développement, lancement payant visé le lundi 7 décembre 2026.

## Le verdict : Pas encore

Calculé par l'outil (`compile.py`), pas écrit à la main :
- ✓ Chaque couple-mois laisse **4,22 €** après ses propres coûts (contribution 53 %).
- ✓ L'année 1 fait **4 141 €** de résultat d'exploitation sur 11 101 € de revenus, avec 149 €/mois de frais fixes et personne de payé ; seuil de rentabilité ≈ 36 couples payants ; mise de 2 040 € remboursée au mois 9.
- ✗ **17 % des acheteuses simulées achètent** (5 sur 30), sous la barre de 25 %. L'offre d'origine faisait 0 sur 20.

Ce qui doit changer, et quel skill le change : le taux d'achat, et il ne dépend plus du prix ni de l'essai (réglés par `/founder-offer` et `/founder-pricing`) mais du **partenaire** : 22 refus sur 25 disent « il ne fera jamais sa part ». C'est `/founder-launch` (50 couples réels, taux d'invitation acceptée) et un `/founder-offer` v3 (mode solo en attendant l'autre, lettre au partenaire, premiers jeux légers) qui tranchent. Les projections reposent sur une montée à 220 couples payants en un an, soit 700 à 1 300 tests terminés par mois ; le site en faisait moins de 20 à mi-septembre. Tant que de vrais couples n'ont pas prouvé mieux, le verdict reste Pas encore.

## Où le board et le panel sont d'accord, et où ils divergent

D'accord sur l'essentiel : le besoin est réel, le test gratuit est l'actif (toutes les acheteuses le feraient), la distribution n'est pas prouvée, et le produit vend une habitude quotidienne à deux sur un site web sans app. Le board (2 PASS, 1 FUND IF, 3,7/10) voulait un prix plus haut et une promesse plus forte ; le panel a fixé un plafond de 12 €/mois et préféré un prix **par couple**. La réconciliation : un seul produit, le Duo, 9,90 € pour deux, c'est plus par personne que l'Essentiel supprimé et sous le seuil de rejet. Le board jugeait le marché difficile à joindre ; le panel le confirme autrement : l'acheteuse est joignable, c'est l'utilisateur indispensable, son partenaire, qui ne l'est pas.

## Le plus gros risque et ce qu'on en fait

**Le partenaire ne vient pas.** Réponse : l'essai de 14 jours ne démarre que quand les deux ont fait le test (on ne paie jamais pour un absent), le partenaire fait sa part en 15 minutes sans compte « pour comparer », les premiers soirs sont des jeux, et le marketing s'adresse à lui autant qu'à elle. Mesure : taux d'invitations acceptées ≥ 30 % sur les 50 couples bêta ; en dessous, on ajoute le mode solo avant de dépenser les 600 € de janvier.

Deuxième risque : la concurrence copie vite (Paired est déjà en français, à 6,25 €/mois en annuel). Le créneau est étroit mais vide : bilan + programme par dimensions, en français, sous 10 €, sans app, test gratuit complet et résiliation en un clic, à l'inverse des deux reproches n°1 du marché.

## Ce qu'il faut pour démarrer

- **Cash : ≈ 2 190 €** (1 750 € de pub déjà budgétés + 230 € de marque INPI + deux mois de frais fixes). Pas de salaire : avec 500 €/mois chacun, l'année 1 perdrait 7 900 €.
- **Avant tout encaissement** : une structure juridique (micro-entreprise ou SAS à deux, voir `ops.md`), le SIRET sur Stripe, les CGV, la migration de domaine.
- **Le premier test réel** (`launch.md`) : pré-vente de l'offre fondateurs à 49 €/an auprès des 50 couples bêta, ligne de succès **10 couples payants avant le 7 décembre**.

## La chose à faire cette semaine

Créer la structure juridique sur le guichet unique (c'est le chemin critique du 7 décembre) et envoyer le lien du test à 10 couples amis en demandant au **partenaire** de le faire de son côté : le taux de retour de ces 10 partenaires dira, avant d'écrire une ligne de code de plus, si le Duo peut se vendre.

*Le panel est fait d'acheteuses simulées et les chiffres sont des projections ; ce sont les vrais couples et les vrais devis qui les confirment. Ce document n'est pas un conseil financier, juridique ni fiscal.*
