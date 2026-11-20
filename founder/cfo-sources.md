# Sources et hypothèses du CFO (numbers.json)

Tout ce qui n'est pas une facture des fondateurs est marqué **estimation** ou **prix public**. Les prix publics sont ceux affichés au 19/11/2026 ; à revérifier sur la page au moment de payer. Pas un conseil comptable, fiscal ni juridique : un expert-comptable doit valider la structure et les cotisations avant le premier encaissement.

## L'unité et le prix
- **Unité** : un « couple-mois » = un mois d'abonnement Duo payé par un couple (deux comptes, un paiement). Choix issu du panel v1 (`panel-v1/results.md`) : les acheteuses refusent de payer 19,90 € pour un partenaire incertain et jugent 9,90 € « par personne » comme « le prix de Netflix ». L'offre v2 (`offer.md`) vend donc un seul produit, le Duo, au prix couple.
- **Prix de base 7,90 €** : moyenne pondérée estimée entre le mensuel à 9,90 € (60 % des couples) et l'annuel à 59 €/an soit 4,92 €/mois (40 %) → 7,91 €. **Estimation** à remplacer par le mix réel Stripe après 3 mois. Les variantes 4,90 / 9,90 / 12,90 sont dans `pricing.md`.
- **TVA** : base en micro-entreprise sous franchise de TVA (seuil services 2025 : 37 500 € de CA, [service-public.fr, franchise en base de TVA](https://entreprendre.service-public.fr/vosdroits/F21746)). Tant que la franchise s'applique, le prix TTC affiché est encaissé en entier. Au-delà du seuil, ou en société à l'IS, la TVA de 20 % s'applique aux abonnements B2C : 9,90 € TTC = 8,25 € HT. **À confirmer avec un comptable.**

## Coûts variables (par couple-mois)
| ligne | montant | source |
|---|---|---|
| Frais Stripe | 1,5 % + 0,25 € par paiement carte UE standard | [stripe.com/fr/pricing](https://stripe.com/fr/pricing), prix public |
| Affiliation | 30 % de l'abonnement pendant 12 mois pour les clients apportés par un praticien ou une créatrice (décision des fondateurs). **Estimation** : 50 % des clients viendront par affiliation → 15 % du CA en moyenne. Le what-if « 100 % affilié » (30 %) est dans `cfo.md`. | fiche contexte fondateurs |
| Cotisations sociales micro-entreprise | ≈ 25,6 % du CA encaissé (taux BNC prestations de services, [urssaf.fr, auto-entrepreneur](https://www.autoentrepreneur.urssaf.fr/portail/accueil/sinformer-sur-le-statut/lessentiel-du-statut.html)). **À vérifier** : le taux dépend de la nature de l'activité retenue (BIC 21,2 % ou BNC 25,6 % en 2026) et de l'ACRE la première année (exonération de 25 % depuis le 1er juillet 2026, sur demande). | prix public, estimation |
| E-mails | ≈ 35 e-mails/mois par couple (rappel quotidien + transactionnels) ; Brevo ou Resend : négligeable sous 20 000 e-mails/mois | [brevo.com/fr/pricing](https://www.brevo.com/fr/pricing/), prix public |

## Coûts fixes mensuels
| ligne | montant | source |
|---|---|---|
| Vercel Pro | 20 $/mois ≈ 18,50 € ; le plan Hobby interdit l'usage commercial | [vercel.com/pricing](https://vercel.com/pricing), prix public |
| Supabase Pro | 25 $/mois ≈ 23 € (le plan gratuit met les projets en pause après inactivité, sans sauvegardes) | [supabase.com/pricing](https://supabase.com/pricing), prix public |
| Outil d'e-mailing | Brevo Starter ≈ 9 €/mois (ou gratuit sous 300 e-mails/jour au début) | prix public |
| Domaines | mylovelab.fr + myrelation.fr ≈ 24 €/an | estimation (prix registrar) |
| IA pour le développement et le contenu | **Estimation** 90 €/mois (abonnement Claude Max 5x ≈ 100 $) ; mettre 20 € si Claude Pro suffit | [claude.com/pricing](https://claude.com/pricing), prix public |
| Banque pro en ligne | ≈ 9 €/mois (Shine, Qonto Basic…) ; une micro-entreprise sous 10 000 € de CA peut utiliser un compte courant dédié gratuit | prix public, estimation |
| Salaires fondateurs | 0 € : les deux cofondateurs ne se paient pas (décision des fondateurs). Le temps de Laurène (15 h/semaine) et de Jules n'est pas valorisé ; à 12 €/h cela représenterait ≈ 780 €/mois non comptés. | fiche contexte |

Non inclus, à ajouter si les fondateurs le décident : assurance RC pro (≈ 10–20 €/mois), comptable (0 € en micro, 30–80 €/mois en société), outils SEO, Canva Pro, WhatsApp Business API si retenu (≈ 0,03–0,05 € par message marketing, voir `ops.md`).

## Dépenses de départ (startup)
| ligne | montant | source |
|---|---|---|
| Publicité | 150 € (Noël) + 600 € (janvier) + 1 000 € (Saint-Valentin) = 1 750 € | fiche contexte fondateurs |
| Dépôt de marque INPI | 230 € pour 2 classes (41 + 44 ; 190 € la première, 40 € par classe supplémentaire) | [inpi.fr, tarifs](https://www.inpi.fr/tarifs), prix public |
| Création de micro-entreprise | 0 € (guichet unique) ; CGV/mentions légales : 60 € **estimation** si un modèle payant est acheté | [formalites.entreprises.gouv.fr](https://formalites.entreprises.gouv.fr), prix public |

Alternative SAS à deux associés : ≈ 200–300 € de création (annonce légale + greffe) + comptable ≈ 50 €/mois ; aucune cotisation sociale sans salaire mais IS de 15 % puis 25 % sur le bénéfice. À comparer avec un comptable si le CA dépasse ~2 000 €/mois.

## Volume : plan et montée en charge
- **Plan** : 10 couple-mois par jour = 300 couples actifs payants. **Estimation**, cohérente avec l'objectif des fondateurs (3 % de paiement) appliqué à ≈ 10 000 tests/mois, ce que le site est loin de faire (moins de 20 tests à mi-septembre). C'est l'hypothèse la plus fragile du dossier.
- **Montée en charge** (couples actifs par mois, ÷ 30 pour les unités/jour) : M1 déc. 10 (les 10 fondateurs payants visés), M2 25, M3 (Saint-Valentin) 60, M4 80, M5 95, M6 110, M7 125, M8 140, M9 160, M10 180, M11 200, M12 220. Hypothèse : chaque vague de pub et le SEO apportent 20 à 40 nouveaux couples par mois, churn mensuel 15 %. **Estimation** à remplacer par les chiffres Stripe réels dès M2.
- **Vérification par le panel** : le panel v1 a acheté à 0 %, le panel v2 (offre corrigée) est dans `panel/results.md`. Un taux d'achat simulé est une borne haute ; la montée en charge ci-dessus suppose que le tunnel réel atteigne 3 % de paiement sur les tests terminés, ce qui reste à prouver avec les 50 couples bêta.
- Pas de capacité physique : aucune limite `capacity_per_day`.
