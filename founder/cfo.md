# La note du CFO

Tout chiffre ci-dessous vient de `numbers.json` passé dans l'outil (sortie brute plus bas) ou d'un what-if relancé avec le même outil. Les sources et les estimations sont dans `cfo-sources.md`. Base : micro-entreprise en franchise de TVA, fondateurs non payés, prix moyen 7,90 € par couple-mois (mix estimé mensuel 9,90 € / annuel 59 €). Pas un conseil comptable, fiscal ni juridique : un expert-comptable doit valider la structure, les cotisations et la TVA avant le premier encaissement.

## La marge
- **Contribution : 4,22 € par couple-mois (53 %)** après Stripe (0,37 €), affiliation moyenne (1,19 €), cotisations sociales micro 2026 (2,02 €) et e-mails (0,10 €).
- **Marge au plan (300 couples actifs) : 47 %.** Coûts fixes 149 €/mois seulement, parce que personne n'est payé.
- **Seuil de rentabilité : 2 couple-mois par jour, soit ≈ 36 couples payants.** En dessous, le site perd ~150 €/mois.

## La ligne à surveiller : le volume, pas le prix
- Le what-if « prix −10 % » coûte 1 100 € sur l'année ; « volume −20 % » en coûte 1 200 € ; « volume −50 % » ramène le profit an 1 à 1 176 € et la mise n'est pas remboursée dans l'année.
- La montée en charge (10 couples en décembre → 220 en novembre 2027) suppose 20 à 40 nouveaux couples payants par mois avec 15 % de churn. Le panel v2 achète à 17 % (borne haute, simulée) et l'objectif réel des fondateurs est 3 % de paiement sur les tests terminés : il faut donc **≈ 700 à 1 300 tests terminés par mois** pour tenir la courbe, contre moins de 20 à mi-septembre. C'est l'hypothèse qui décide de tout ; les 50 couples bêta diront si elle tient.
- Deuxième ligne : **l'affiliation**. Si 100 % des clients viennent par des créatrices ou des praticiens à 30 %, la contribution tombe à 3,17 € (40 %), la marge au plan à 34 %, le profit an 1 à 2 665 €. Supportable, mais 30 % sur 12 mois est généreux pour un prix de 7,90 € : prévoir de passer à 30 % sur 6 mois ou 20 % sur 12 mois une fois les 10 premières affiliées signées.
- Troisième ligne : **les cotisations**. Le taux micro BNC 2026 est de 25,6 % (21,2 % si l'activité est classée BIC) et l'ACRE n'exonère plus que 25 % la première année et n'est plus automatique (`ops.md`) : le classement BNC/BIC vaut ± 0,35 € par couple-mois, à trancher avec l'URSSAF et un comptable avant le 7 décembre.

## Cash
- **Cash nécessaire avant que ça se paie tout seul : ≈ 2 190 €**, atteint au mois 2 ; c'est la mise de départ (1 750 € de pub + 230 € INPI + 60 €) plus deux mois de frais fixes.
- Mise remboursée au **mois 9** (août 2027). Profit an 1 : 4 141 € sur 11 101 € de revenus ; 2 101 € après la mise.
- Ce que le modèle ne paie pas : le temps des fondateurs. Avec 500 €/mois chacun, le seuil passe à 10 couple-mois/jour (≈ 300 couples), la marge au plan à 5 %, et l'année 1 perd 7 859 €. **MyLoveLab n'est pas encore une entreprise qui rémunère ; c'est un projet qui s'autofinance à partir de 36 couples.**

## Trois façons d'améliorer la marge (chiffrées avec l'outil)
1. **Pousser l'annuel au lieu du mensuel ne l'améliore pas** : à 4,90 € de prix moyen (100 % annuel), le profit an 1 tombe à 1 821 €. L'annuel sert à la trésorerie et à la rétention, pas à la marge. Garder le mensuel visible.
2. **Monter le mensuel à 12,90 €** (prix moyen ≈ 9,90 €) : contribution 5,52 €, profit an 1 5 939 €, +1 700 €. À tester en A/B (`pricing.md`), dans la fourchette du panel.
3. **Plafonner l'affiliation à 6 mois** : si la moitié des clients sont affiliés, la commission moyenne passe de 15 % à ~7,5 % après le premier semestre, soit +0,60 € par couple-mois, ≈ +800 € sur l'année à volume égal.

## Les conditions du board sur l'argent
- « Coût d'acquisition supportable » : avec 4,22 € de contribution et 7 mois de rétention moyenne (churn 15 %), un couple vaut ≈ 30 € de contribution. **Le maximum à payer pour un couple payant est 30 € ; viser 10 €.** À 3 % de paiement, cela veut dire au plus 0,90 € par test terminé, 0,30 € visé. Les 600 € de janvier doivent donc produire au moins 20 couples payants pour ne pas être perdus, 60 pour être rentables (`marketing.md`).
- « Entité juridique avant encaissement » : non chiffrée ici, la micro-entreprise est gratuite à créer ; voir `ops.md`.
- « Le prix testé, pas décrété » : fait, `pricing.md`.

## Sortie de l'outil
# Unit economics: MyLoveLab (abonnement couples, France) — base : micro-entreprise en franchise de TVA, prix TTC = HT

Every number below comes from the input file. Nothing is looked up or guessed.

## One couple-mois (un mois de Duo payé par un couple, mix mensuel 9,90 € / annuel 59 €)

| line | per couple-mois (un mois de Duo payé par un couple, mix mensuel 9,90 € / annuel 59 €) |
| --- | ---: |
| Price | € 7.90 |
| Frais Stripe (1,5 % + 0,25 € par paiement carte UE, sur 7,90 €) | -€ 0.37 |
| Commission d'affiliation (30 % sur 12 mois, estimée sur 50 % des clients = 15 % en moyenne) | -€ 1.19 |
| Cotisations sociales micro-entreprise BNC 2026 (25,6 % du CA encaissé, à vérifier ; 21,2 % si BIC) | -€ 2.02 |
| E-mails de rappel et transactionnels (≈ 70/mois pour deux comptes) | -€ 0.10 |
| **Contribution** (what each couple-mois (un mois de Duo payé par un couple, mix mensuel 9,90 € / annuel 59 €) leaves to pay the fixed costs) | **€ 4.22** (53%) |

## The margin that matters

Fixed costs: € 149 a month (Vercel Pro (hébergement, usage commercial) € 18, Supabase Pro (base, auth, sauvegardes) € 23, Outil d'e-mailing (Brevo, gratuit sous 300 e-mails/jour puis Starter ≈ 7 € HT) € 7, Noms de domaine mylovelab.fr + myrelation.fr (≈ 19 €/an) € 2, Abonnement IA pour le développement et le contenu (Claude, estimation) € 90, Banque pro en ligne pour micro-entreprise (estimation) € 9, Salaires fondateurs € 0).

- **Break-even: 2 couple-mois (un mois de Duo payé par un couple, mix mensuel 9,90 € / annuel 59 €)s a day.** Below that you lose money every month.
- **Profit margin at your plan** (10 a day): **47%** of every sale, after every cost.

## Year 1, month by month

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

## What if

| scenario | margin at plan | break-even a day | year 1 profit |
| --- | ---: | ---: | ---: |
| Base plan | 47% | 2 | € 4,141 |
| Price -10% | 41% | 2 | € 3,031 |
| Volume -20% | 46% | 2 | € 2,955 |
| Unit costs +15% | 40% | 2 | € 3,365 |

No red flags in these numbers. They are only as good as the inputs: check every cost against a real quote.
