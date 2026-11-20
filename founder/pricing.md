# Prix : ce que les acheteuses disent, ce que les concurrents facturent, ce dont l'entreprise a besoin

Sources : `pricing-curve.md` (20 réponses de prix du panel v1, offre à 9,90 € solo / 19,90 € Duo), `competitors.md`, `numbers.json` passé dans l'outil du CFO à quatre prix. Les réponses de prix viennent d'acheteuses simulées : elles servent à choisir quoi tester, pas de preuve.

## 1. Ce que les acheteuses ont dit (Van Westendorp, 20 réponses, en €/mois)

| point | prix | sens |
|---|---:|---|
| PMC | 3,02 € | en dessous, « trop bon marché pour être sérieux » |
| OPP | 3,04 € | le moins de résistance dans les deux sens |
| IPP | 6,02 € | autant trouvent que c'est une bonne affaire que cher |
| PME | 12,03 € | au-dessus, trop de refus |

Fourchette acceptable : **3 € à 12 € par mois**. Médianes : trop bon marché 2 €, bonne affaire 5 €, cher 12 €, trop cher 20 €. Le 9,90 € solo est dans la fourchette, dans son tiers haut. **Le Duo à 19,90 € est au-dessus du seuil de rejet** (PME 12 €), et c'est précisément le plan que les acheteuses considèrent, puisqu'aucune ne voit l'intérêt de payer seule pour un rituel à deux. En re-test (panel v2, prix 9,90 € pour deux), les réponses restent dans la même zone : bonne affaire 4–5 €, cher 10–12 €, trop cher 15–20 € ; une acheteuse a répondu en annuel (bonne affaire 49 €, cher 79 €, trop cher 120 €).

## 2. Ce que les concurrents facturent (pour le couple, un seul abonnement)

| | mensuel | annuel ramené au mois |
|---|---:|---:|
| Paired (FR, app) | 14,99 € | 6,25 € (74,99 €/an) |
| UpLuv (fiche FR) | 9,99 $ | 5,00 € (59,99 €/an) |
| LovBirdz (FR, Nantes) | 6,99 € | 2,08 € (24,99 €/an) |
| Coral / Flamme (EN) | 12,99 $ | 3,75–5 $ |
| Evergreen (EN) | — | 4,17 € (49,99 €/an) |
| Lasting (EN, le plus proche du « bilan + programme ») | 29,99 $ | 15 $ (89,99 $/6 mois) |
| Gottman Connect (EN, web) | achat unique 139–169 $ | — |
| Thérapie de couple (France) | 60–150 € la séance | — |

Lecture : les leaders incluent le partenaire dans un seul abonnement ; la médiane des mensuels est ≈ 13 $, celle des annuels ≈ 5 €/mois. Un Duo à 19,90 € serait le produit le plus cher du marché grand public ; un Essentiel « par personne » n'a pas d'équivalent chez les leaders.

## 3. Ce dont l'entreprise a besoin (outil du CFO, unité = couple-mois, coûts en % recalculés à chaque prix)

| prix du couple-mois | contribution | marge au plan (300 couples) | seuil de rentabilité | profit an 1 | retour sur la mise |
|---:|---:|---:|---:|---:|---|
| 4,90 € (annuel seul à 59 €) | 2,59 € (53 %) | 43 % | 2 /jour ≈ 59 couples | 1 821 € | pas dans l'année |
| 7,90 € (mix 60 % mensuel / 40 % annuel) | 4,35 € (55 %) | 49 % | 2 /jour ≈ 35 couples | 4 295 € | mois 9 |
| 9,90 € (mensuel seul) | 5,52 € (56 %) | 51 % | 1 /jour ≈ 28 couples | 5 939 € | mois 8 |
| 12,90 € | 7,30 € (57 %) | 53 % | 1 /jour ≈ 21 couples | 8 440 € | mois 7 |

Les coûts fixes sont de 149 €/mois et les fondateurs ne se paient pas : tout prix au-dessus de 5 € couvre les frais dès 30 à 60 couples. Le prix ne décide pas de la survie ; le volume, oui. Ce que le prix décide, c'est le coût d'acquisition supportable (voir `marketing.md`) et la crédibilité.

## 4. Décision

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

## 5. Les objections de prix du panel, mot pour mot (pour le marketing)
1. « 9,90 € par mois pour un site c'est le prix de Netflix, que je regarde tous les soirs, lui. » (P002)
2. « 19,90 € par mois pour la version à deux, avec le bébé et mon salaire, c'est le prix des couches du mois ; et la version à 9,90 € toute seule, ça n'a aucun sens pour un rituel de couple. » (P006)
3. « Un vrai essai gratuit du Duo d'une quinzaine de jours après le test, ou un format à acheter une fois (genre un pack de niveaux à 15–20 €, comme un jeu de cartes) plutôt qu'un mensuel. » (P006, ce qui la ferait changer d'avis)

Le prix a changé par rapport à `idea.md` : `numbers.json` est à jour (prix de base 7,90 € = mix estimé), le CFO est relancé dans `cfo.md`.
