# Le board : synthèse de la présidence

Trois membres, trois lentilles (Offers, Monopoly, Product), un même brief (`board/brief.md`). Les mémos complets sont dans `board/offers.md`, `board/monopoly.md`, `board/product.md`.

## 1. Le vote

**2 PASS, 1 FUND IF. Score moyen : 3,7 / 10** (Offers 4, Monopoly 3, Product 4).

Le board ne finance pas MyLoveLab tel qu'il est documenté aujourd'hui. Aucun membre n'a jugé l'idée mauvaise ni le besoin faux ; tous trois ont jugé que l'entreprise n'a pas encore apporté la preuve qu'elle sait atteindre son acheteuse et la faire revenir. Un PASS est un résultat, pas un échec : il dit ce qu'il reste à prouver, et les trois lentilles sont d'accord sur ce que c'est.

## 2. Les risques soulevés par plus d'un membre (dans l'ordre)

1. **Aucune distribution prouvée** (Offers, Monopoly, Product). Moins de 20 tests passés à mi-septembre, chiffre actuel inconnu, zéro couple payant, canaux froids en échec, 4 praticiens positifs sur 160, 1 750 € de pub sur trois vagues. Les 100 premiers couples payants n'ont pas de chemin décrit ni de coût connu. C'est le risque n° 1 des trois mémos.
2. **Pas de preuve que ça marche** (Offers, Product). Citer Gottman ou Sue Johnson n'est pas une preuve que ces sessions produisent un résultat pour ce couple. Pas d'avant/après, pas de rétention mesurée, pas de garantie. L'acheteuse n'a aucune raison de croire.
3. **L'habitude quotidienne sur un site web, sans app ni notification native** (Offers, Monopoly, Product). Le produit vend « quelques minutes par jour » mais le moment critique, le lendemain matin, n'est pas conçu. Les concurrents sont dans la poche de l'utilisatrice.
4. **Le prix plafond de 10 €/mois comme principe** (Offers, Monopoly). Être moins cher que Paired n'est pas un positionnement ; combiné à 30 % d'affiliation et à un faible volume, la marge par couple ne finance pas la distribution qui manque.
5. **Pas de douve** (Monopoly, implicitement Offers). Base scientifique publique, contenu reproductible avec les mêmes outils d'IA ; rien n'empêche une copie au sixième mois.
6. **Trop de briques pour 15 h/semaine** (Product, Offers). Cartes-questions, calendrier, podcasts, anglais, carte cadeau : tout cela avant que la boucle test → session → retour ne soit mesurée.
7. **Les coutures et le cadre** (Product). Test anonyme → compte → invitation → Stripe → session à deux, plus une migration de domaine et un lancement payant sans entité juridique.

Désaccord à garder : le Product lens croit que la boucle produit peut tenir si elle est resserrée (FUND IF), là où Offers et Monopoly jugent que le marché lui-même (demande latente, acheteuse difficile à joindre) est le problème et que le resserrage du produit ne suffira pas. Les deux lectures sont compatibles : la seconde se tranche avec des chiffres que la première exige aussi.

## 3. Les conditions, fusionnées en checklist

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

## 4. La version la plus forte de cette entreprise, vue du board

Ce n'est pas « une app de couple moins chère que Paired ». C'est **le test de couple de référence en français**, gratuit, anonyme, fondé sur la recherche, qui arrive au bon moment (le soir d'une dispute, via Google et un reel de psy) et qui produit en 15 minutes quelque chose que l'on veut montrer à l'autre. Le produit payant est ensuite le **Duo** : deux regards côte à côte, une question du jour, une action à tester ce soir ; vendu plus cher que prévu, à deux, avec une promesse datée et une garantie, et distribué par les praticiens et les créatrices qui y envoient leurs couples. Le mobile se traite par une PWA installable et un rappel quotidien par e-mail ou WhatsApp, pas par une app native. Tout le reste (cartes, calendrier, podcasts, anglais) attend que la boucle test → Duo → retour le lendemain soit mesurée sur 50 couples. Cette version diffère de ce que les fondateurs ont présenté sur trois points : le prix (plus haut, pas plus bas), l'objet vendu (le Duo, pas l'abonnement solo) et la feuille de route (une boucle, pas dix briques).

*Note de la présidence : le brief a été rédigé avant lecture du site. Le site confirme que le test est déjà gratuit, anonyme et sans compte, que le Mode Duo existe déjà en bêta gratuite, et qu'il y a 17 articles de blog, 6 jeux à deux et 18 pages « recherche ». Cela renforce le point 4 (l'actif, c'est le test et le contenu) et le point 6 (beaucoup de briques existent déjà).*
