# Rapport SEO hebdomadaire — intelligenceproduit.com
**Date de l'audit :** 24 août 2026
**Audité par :** Intelligence Produit SEO Bot (tâche planifiée)
**Audit précédent :** 17 août 2026

---

## Résumé exécutif

| | |
|---|---|
| **Score global SEO** | 🟡 **Moyen** |
| **Évolution vs 17 août** | ↑ **Progrès majeur** — le problème critique est résolu |
| **Problème critique du 17 août** | ✅ **CORRIGÉ** — le titre "Maquette home (style réel)" a disparu de la production |
| **Blocage restant** | Indexation Google toujours à zéro |

Le déploiement Cloudflare Pages est enfin aligné sur les fichiers locaux. La homepage en production affiche désormais le bon titre, la bonne meta description, le bon canonical et la balise de vérification Search Console. C'est la correction la plus importante des quatre dernières semaines et elle est faite.

Il reste un seul verrou : le site n'apparaît toujours dans aucun résultat de recherche. Ce n'est plus un problème de contenu ou de balisage — c'est un problème d'indexation et d'autorité de domaine. Le site est neuf, il n'a quasiment aucun backlink, et Google n'a pas encore de raison de le crawler en profondeur.

---

## Indexation

| Indicateur | Résultat | Évolution |
|---|---|---|
| Pages indexées (`site:intelligenceproduit.com`) | **0** — aucun résultat retourné | = (identique au 17 août) |
| Sitemap accessible | ✅ Oui | = |
| URLs dans le sitemap | **19** (6 pages principales + 13 articles) | = |
| Problème www vs apex | Non détecté — apex uniquement | = |
| robots.txt | ✅ Correct, `Allow: /` + directive Sitemap + Content-Signal | = |

**Note méthodologique :** l'opérateur `site:` via l'API de recherche utilisée n'est pas un substitut fiable à Google Search Console. Un résultat vide ne prouve pas formellement une indexation nulle. La vérification dans Search Console reste indispensable — c'est la recommandation n°1 depuis trois semaines et elle n'a toujours pas été confirmée faite.

**Point positif :** `article-speedboat.html` existe localement mais reste absent du sitemap (signalé le 3 août, toujours non corrigé). 14 articles en local, 13 dans le sitemap.

---

## Mots-clés et positions

| Mot-clé | Position estimée | URL positionnée | Évolution | Notes |
|---------|-----------------|-----------------|-----------|-------|
| conseil produit PME | Non classé | — | = | Concurrents : Egnoka, Advyse, PMI Conseils, Pro PME |
| coach produit PME PMI | Non classé | — | = | SERP dominée par le coaching de dirigeants, pas le produit |
| consultant product management PME | Non classé | — | = | Résultats anglophones (Toptal, PMX Group) |
| management produit PME Lyon | Non classé | — | = | Sortlist, Flexilab, Kreapp, Alkemys occupent le terrain |
| coach en management produit | Non classé | — | = | Opilus et Thiga dominent — cible tech/startup, pas PMI |
| diagnostic produit PME | Non classé | — | = | Scale2Sell, Cap Performances |
| diagnostic 360 produit industriel | Non classé | — | **nouveau (testé)** | ⚠️ GAYA Conseil est positionné avec une page dédiée "Diagnostic 360° pour PME industrielles" — concurrent direct |
| pourquoi mon produit ne se vend pas PME | Non classé | — | = | SERP faible qualité (forums, Facebook) — **opportunité réelle** |
| product manager PME externalisé | Non classé | — | = | Aucun acteur français fort |
| accompagnement lancement produit PME France | Non classé | — | = | Bpifrance / France 2030 monopolisent |
| redéfinir produit industriel PME | Non classé | — | **nouveau (testé)** | Bpifrance, aides publiques — pas de concurrent conseil |
| consultant produit Lyon PME | Non classé | — | = | KSTN, Egnoka, MD Consulting, Otago |
| intelligence produit PME | Non classé | — | = | Google lit "intelligence artificielle" / "intelligence économique" |

**Recherche de marque :** une requête `"intelligence produit" Grégoire Gérard conseil PME` fait remonter le **profil LinkedIn** de Greg en position 1 — mais pas le site. Le LinkedIn capte l'autorité de marque que le site devrait capter.

---

## Analyse on-page — page d'accueil (version LIVE)

| Élément | Statut | Valeur constatée en production |
|---------|--------|-------------------------------|
| `<title>` | ✅ **Corrigé** | `Conseil Produit PME/PMI — Intelligence Produit \| Lyon` |
| `<meta name="description">` | ✅ Conforme | Texte attendu, mot pour mot |
| `<link rel="canonical">` | ✅ Correct | `https://intelligenceproduit.com/` |
| `og:url` | ✅ Correct | `https://intelligenceproduit.com/` |
| `og:title` / `og:description` / `og:image` | ✅ Présents | Image `hero-greg.jpg` |
| `google-site-verification` | ✅ Présent | `sFqfrB0wOUs0E_mQCDwT9U2cfhQq-4rxvGYKXAFKelo` |
| JSON-LD `ProfessionalService` | ✅ Présent | Nom, URL, logo, fondateur + LinkedIn, adresse Tassin, areaServed FR |
| `<h1>` | ⚠️ Sans mot-clé | "Encore un consultant ? Non." |
| Structure `<h2>` | ⚠️ Faible | Un seul H2 ("Un problème produit précis en tête ?") ; 3 H3 et 3 H4 |

### Canonicals sur l'ensemble du site — ✅ propres
Les 6 pages principales et les 14 articles portent tous un canonical auto-référent sans extension `.html`. Aucune incohérence détectée.

### ⚠️ Nouveau point relevé cette semaine : maillage interne non canonique
Tous les liens de navigation pointent vers les URLs **avec** `.html` (`/qui-suis-je.html`, `/offres.html`…), alors que les canonicals et le sitemap déclarent les versions **sans** extension (`/qui-suis-je`). Cloudflare Pages sert les deux, donc le contenu est accessible en double.

Concrètement : Google découvre d'abord les URLs `.html` par le maillage, doit ensuite suivre le canonical vers l'URL sans extension, et gaspille du budget de crawl sur un site qui n'en a déjà pas beaucoup. Le logo, présent sur toutes les pages, pointe vers `/index.html` alors que le canonical de la home est `/`.

Ce n'est pas fatal, mais sur un site en phase d'amorçage d'indexation, ça envoie un signal brouillé au pire moment.

---

## Points forts

- **Le blocage n°1 est levé.** Après trois audits consécutifs signalant le titre "Maquette", la production est enfin conforme. Tout le travail SEO local est désormais visible par Google.
- **Balisage technique complet et correct** : canonical, og:*, JSON-LD ProfessionalService, google-site-verification, robots.txt avec directive Sitemap et Content-Signal (autorisation explicite aux agents IA).
- **14 articles de fond** couvrant un vocabulaire sémantique cohérent : diagnostic 360°, Ishikawa, AMDEC, 5 pourquoi, chaîne de valeur Porter, objets frontières. C'est un vrai capital éditorial.
- **Page "Qui suis-je" très bien optimisée** : titre porteur ("Entrepreneur & Coach Produit PME"), meta description factuelle avec noms d'entreprises, structure H2 riche, parcours détaillé. C'est la meilleure page du site en l'état.
- **Aucun problème de canonicalisation www/apex.**

## Points d'amélioration

- 🔴 **Indexation toujours nulle.** Le site est propre techniquement mais invisible. Sans confirmation Search Console, on avance à l'aveugle depuis quatre semaines.
- 🔴 **Zéro backlink identifié.** Aucun signal d'autorité externe. Le LinkedIn de Greg se positionne, le site non — la différence, c'est l'autorité de domaine.
- ⚠️ **Maillage interne `.html` vs canonicals sans extension** (nouveau, voir ci-dessus).
- ⚠️ **H1 homepage sans mot-clé.** "Encore un consultant ? Non." fonctionne en accroche, pas en signal SEO.
- ⚠️ **Structure H2 trop plate sur la homepage** : les sections Positionnement, Outils, Articles sont balisées en H3/H4 sans H2 parent, ce qui casse la hiérarchie sémantique.
- ⚠️ **`article-speedboat.html` toujours absent du sitemap** (signalé le 3 août).
- ⚠️ **Aucune page de service dédiée.** "Diagnostic 360° produit industriel" mériterait sa propre page — GAYA Conseil se positionne précisément avec cette stratégie.

---

## Top 3 recommandations pour la semaine suivante

### 1. 🔴 Confirmer l'indexation dans Google Search Console — maintenant que le site est propre

C'est la seule action qui débloque tout le reste, et c'est la troisième semaine consécutive qu'elle est recommandée. Le contexte a changé : avant, demander une indexation aurait fait indexer une page "Maquette". Aujourd'hui la page est bonne.

À faire, dans l'ordre :
- Soumettre `https://intelligenceproduit.com/sitemap.xml` dans Search Console
- Utiliser "Inspecter l'URL" sur la homepage → **Demander une indexation**
- Répéter pour `/qui-suis-je`, `/offres` et `/article-diagnostic-360`
- Relever le nombre de pages "Valides" vs "Exclues" et la raison des exclusions

Sans cette étape, les audits suivants continueront à rapporter zéro sans pouvoir en expliquer la cause.

### 2. Aligner le maillage interne sur les canonicals

Remplacer dans les 20 fichiers HTML les liens `href="xxx.html"` par `href="/xxx"`, et le lien du logo `index.html` par `/`. Une passe de recherche-remplacement suffit.

Bénéfice : Google crawle directement les bonnes URLs, plus de dilution, budget de crawl préservé. Sur un site en amorçage, ça compte.

À faire dans la même passe : ajouter `article-speedboat` au sitemap.

### 3. Créer une page dédiée "Diagnostic 360° produit industriel"

C'est le mot-clé où la concurrence est la plus lisible et la plus battable : GAYA Conseil occupe le terrain avec exactement ce format de page, et le reste de la SERP est occupé par des CCI qui proposent un diagnostic de compétitivité généraliste, pas produit.

L'angle différenciant est déjà écrit dans l'article `article-diagnostic-360.html` — il s'agit de le transformer en page de service : `/diagnostic-360-produit-industriel`, avec H1 portant le mot-clé exact, description de la méthode (Porter + Ishikawa + données SAV), livrables, durée, et un CTA Calendly.

Cible secondaire à couvrir dans la même page ou en article suivant : **"pourquoi mon produit ne se vend pas"** — la SERP y est faible (forums, posts Facebook), c'est la porte d'entrée la plus accessible du portefeuille de mots-clés.

---

## Suivi des recommandations précédentes

| Recommandation (17 août) | Statut |
|---|---|
| 1. Redéployer la bonne version du site | ✅ **Fait** |
| 2. Vérifier l'indexation dans Search Console | ❓ Non confirmé — reportée |
| 3. Ajouter les mots-clés dans H1/H2 de la homepage | ❌ Non fait |

---

*Prochain audit prévu : semaine du 31 août 2026*
