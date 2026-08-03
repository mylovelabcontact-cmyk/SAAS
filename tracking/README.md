# Tracking — Microsoft Clarity & Google Analytics 4

Ce dossier contient les snippets officiels de tracking à intégrer dans le
`<head>` global du site :

| Outil | Identifiant |
|---|---|
| Microsoft Clarity | `wu92rr32yp` |
| Google Analytics 4 | `G-CE0CDHM7KM` |

## Pourquoi ce fichier et pas une intégration directe ?

Au moment de cette contribution, le dépôt ne contenait **aucun code de site**
(aucun commit sur aucune branche). Il n'était donc pas possible d'injecter les
balises directement dans un layout existant. Le fichier
[`head-tracking.html`](./head-tracking.html) contient les snippets prêts à
coller.

## Comment intégrer

Coller le contenu de la version choisie de `head-tracking.html` dans le
`<head>` du **layout partagé par toutes les pages** — y compris la page
d'accès testeur — selon la stack du site :

- **HTML statique** : dans le `<head>` de chaque fichier `.html` (ou du
  template commun s'il y en a un).
- **Next.js (App Router)** : dans `app/layout.tsx` (via `next/script` ou
  directement dans `<head>`).
- **Next.js (Pages Router)** : dans `pages/_document.tsx`.
- **Nuxt / Vue** : dans `nuxt.config.ts` (`app.head.script`) ou `app.vue`.
- **React (Vite/CRA)** : dans `index.html`.
- **WordPress** : dans `header.php` du thème, avant `</head>`.

## Deux versions disponibles

1. **Version standard** : chargement immédiat sur toutes les pages. À
   utiliser s'il n'y a pas de bandeau de consentement cookies.
2. **Version avec consentement** (commentée dans le fichier) : les scripts ne
   se chargent qu'après acceptation des cookies. Le bandeau doit appeler
   `window.loadTrackingScripts()` au clic sur « Accepter ». Google Consent
   Mode v2 est configuré en `denied` par défaut. Adapter la clé
   `localStorage` (`cookieConsent`) à celle utilisée par votre bandeau.
