# L'offre : du produit à l'offre qu'on ne refuse pas facilement

Méthode : la lentille Offers (`../jakeschincariol/founder-skill/skills/founder-board/lenses.md`, résumé du cadre de *$100M Offers*, jamais présenté comme les mots de l'auteur). Matière première : `panel-v1/results.md` (0 achat sur 20), `competitors.md` (reproches du marché), `board.md` (conditions), `numbers.json` (ce que chaque brique coûte).

## 1. Ce que vendait l'offre d'origine (pitch v1, `pitch-v1.md`)
Test gratuit → Essentiel 9,90 €/mois (une personne) ou Premium Duo 19,90 €/mois, sans essai, site web sans appli. Résultat : 0 achat sur 20. Les acheteuses ont adoré le test et refusé l'abonnement, pour quatre raisons qui reviennent dans 20 réponses sur 20.

## 2. La liste des problèmes (dans les mots des acheteuses)

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

## 3. Les solutions, notées et triées

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

## 4. La pile (ce que voit l'acheteuse)

**Le cœur** : *Le Duo MyLoveLab*. Deux comptes reliés, un seul paiement. Le résultat vendu : « vous comprendre à deux, deux minutes par soir », pas « 420 sessions ».

**Les bonus** (chacun tue une objection)
1. *Vos deux regards* : le test fait chacun de son côté, les scores côte à côte, uniquement quand les deux ont fini (objection 1, 13).
2. *La question du soir dans la notification* : deux minutes, sans ouvrir le site (objection 9, 10).
3. *14 jours offerts, qui ne démarrent que quand vous êtes deux* (objection 4, 11).

**La garantie** : satisfait ou remboursé 30 jours, résiliation en un clic, rappel avant la fin de l'essai. Coût modélisé : à 5 % de remboursements, 0,50 € par nouveau couple, soit 1 % du revenu annuel d'un couple ; à 15 %, 1,50 €. Supportable (contribution 4,22 € par couple-mois, `cfo.md`).

**La rareté** : offre fondateurs, 100 couples, 49 €/an, jusqu'au 31 décembre 2026, prix garanti tant que l'abonnement est actif. Après : 59 €/an. Pas de compte à rebours artificiel, pas de « -30 % Saint-Valentin » (la Saint-Valentin se vend avec la carte cadeau au prix normal).

**Le nom** : « Le Duo » (le produit) et « Offre fondateurs » (le lancement). Pas « Premium », pas « Essentiel ».

## 5. L'équation de valeur, avant / après (1–10)

| | v1 | v2 | ce qui bouge |
|---|:-:|:-:|---|
| Résultat rêvé | 6 | 7 | « vous comprendre à deux » reste le même rêve ; « Vos deux regards » le rend visible |
| Probabilité perçue | 2 | 4 | sources citées, essai gratuit, garantie ; toujours pas de preuve sociale (marque inconnue) |
| Temps avant résultat | 4 | 7 | le premier résultat (les deux regards) arrive le soir même, pas au niveau 10 |
| Effort et sacrifice | 2 | 5 | 2 minutes depuis la notification au lieu de 8 minutes sur un site ; mais l'effort n°1, convaincre le partenaire, reste à la charge de l'acheteuse |

## 6. Le re-test

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

## Règles tenues
Toutes les promesses sont livrables avec ce qui existe sur le site (test sans compte, Duo, jeux) plus trois briques : essai conditionnel Stripe, PWA + web push, e-mails de rappel. Pas de faux avis, pas de faux compte à rebours. La garantie et la résiliation suivent le droit de la consommation français (information précontractuelle, rappel avant reconduction) : à faire relire, pas un conseil juridique.
