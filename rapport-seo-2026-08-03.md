# Rapport SEO Hebdomadaire — intelligenceproduit.com
**Date de l'audit :** 3 août 2026

---

## Résumé exécutif

| Indicateur | Valeur |
|------------|--------|
| Score global SEO | 🟡 Moyen (en progression) |
| Pages indexées Google | 0 — site toujours non indexé en live |
| Sitemap accessible | ✅ Oui — 19 URLs |
| Positionnement mots-clés | Non détecté |
| Évolution vs audit du 31 juillet | ↑ Progrès significatifs sur les fichiers locaux — **mais pas encore déployés** |

**Situation :** Les fichiers locaux ont été nettement améliorés depuis le dernier audit (titre corrigé, canonical ajouté sur toutes les pages, 14 articles présents). Mais la version live sur Cloudflare Pages affiche encore le titre "Maquette home (style réel)", ce qui signifie que **le commit n'a pas encore été poussé sur GitHub**. L'indexation et le positionnement ne s'amélioreront pas tant que ce déploiement n'est pas effectué.

---

## 1. Indexation

### `site:intelligenceproduit.com`
- **Pages indexées : 0** (= audit précédent)
- La recherche Google ne retourne aucun résultat pour le domaine.
- Pas de problème de canonicalisation www vs apex détecté.

### Sitemap local
- **19 URLs présentes** : 6 pages principales + 13 articles.
- ⚠️ **`article-speedboat.html` absent du sitemap** : ce fichier existe localement mais n'est pas référencé dans `sitemap.xml`.
- URLs du sitemap sans extension `.html` (ex : `/qui-suis-je` plutôt que `/qui-suis-je.html`) — Cloudflare Pages gère les clean URLs, donc ce n'est pas bloquant.

### Problème principal : déploiement en attente
La version live affiche encore le titre "Maquette home (style réel)". Le fichier `index.html` local a le bon titre et la balise canonical. **Le push sur GitHub n'a pas encore été effectué.**

---

## 2. Mots-clés et positions

Aucun mot-clé testé ne fait apparaître intelligenceproduit.com dans les résultats — identique à la semaine dernière, ce qui est cohérent avec l'absence d'indexation.

| Mot-clé | Position estimée | URL positionnée | Évolution | Notes |
|---------|-----------------|-----------------|-----------|-------|
| conseil produit PME | Non classé | — | = | Concurrents : advyse, katalyse, gayaconseil |
| coach produit PME PMI | Non classé | — | = | — |
| consultant product management PME | Non classé | — | = | Concurrents majoritairement anglophones |
| management produit PME Lyon | Non classé | — | = | Résultats dominés par formations universitaires |
| coach en management produit | Non classé | — | = | — |
| diagnostic produit PME | Non classé | — | = | Résultats : BPIFrance, cadres-en-or, diag-entreprise |
| diagnostic 360 produit industriel | Non classé | — | = | 🎯 Faible concurrence directe — opportunité |
| pourquoi mon produit ne se vend pas PME | Non classé | — | = | 🎯 Faible concurrence directe — opportunité |
| product manager PME externalisé | Non classé | — | = | Concurrents : lesdigivores.ch, studi |
| accompagnement lancement produit PME France | Non classé | — | = | Résultats dominés par aides publiques / Bpifrance |
| redéfinir produit industriel PME | Non classé | — | = | — |
| consultant produit Lyon PME | Non classé | — | = | Concurrents : kstn.fr, egnoka.fr, mdupreconsulting.com |
| intelligence produit PME | Non classé | — | = | Résultats : IA PME, intelligence artificielle — confusion de niche |

**Observation :** Les mots-clés "diagnostic 360 produit industriel" et "pourquoi mon produit ne se vend pas PME" restent des niches faiblement couvertes par des concurrents directs. L'article `article-diagnostic-360.html` est idéalement positionné pour capter ces requêtes dès l'indexation.

---

## 3. Analyse on-page

### Homepage (index.html — version locale)

| Élément | Statut local | Statut live | Note |
|---------|-------------|-------------|------|
| `<title>` | ✅ "Conseil Produit PME/PMI — Intelligence Produit \| Lyon" | 🔴 "Intelligence Produit — Maquette home (style réel)" | **Corrigé localement, pas déployé** |
| `<link rel="canonical">` | ✅ `https://intelligenceproduit.com/` | ⚠️ Non vérifié en live | **Ajouté depuis le dernier audit** — était absent |
| `<meta name="description">` | ✅ Conforme | ⚠️ Non vérifié en live | OK |
| `og:url` | ✅ `https://intelligenceproduit.com/` | ⚠️ Non vérifié en live | OK |
| `og:title` | ✅ Correct | ⚠️ Non vérifié en live | OK |
| Google Site Verification | ✅ Présent | ⚠️ Non vérifié en live | OK |
| JSON-LD ProfessionalService | ✅ Complet | ⚠️ Non vérifié en live | Adresse, fondateur, périmètre renseignés |
| H1 | ⚠️ "Encore un consultant ? Non." | = | Aucun mot-clé cible |
| H2 | ⚠️ "Un problème produit précis en tête ?" | = | Aucun mot-clé cible |

### Articles

- **Canonical présent sur tous les articles** ✅ — c'est une amélioration depuis le dernier audit.
- **14 articles** présents localement (13 dans le sitemap).
- **Méta descriptions manquantes** sur 10 des 14 articles (présentes uniquement sur : diagnostic-360, objets-frontieres, design-pme, speedboat).

Articles sans meta description :
`article-sales-book`, `article-keep-it-simple`, `article-build-it-yourself`, `article-fmea-amdec`, `article-ishikawa`, `article-5-pourquoi`, `article-chaine-valeur-porter`, `article-diagnostic-combine`, `article-product-manager-entre-2-chaises`, `article-voir-autrement`

---

## 4. Points forts

- ✅ **Titre corrigé localement** — le fichier index.html a le bon titre SEO
- ✅ **Canonical ajouté sur toutes les pages** — progrès majeur depuis l'audit du 31 juillet
- ✅ **14 articles** publiés localement — capital de contenu solide
- ✅ **JSON-LD ProfessionalService complet** sur la homepage
- ✅ **Sitemap complet** avec 19 URLs
- ✅ **Google Site Verification présent** — Search Console opérationnelle
- ✅ **Niches peu concurrencées** disponibles dès indexation (diagnostic 360, pourquoi mon produit ne se vend pas)

---

## 5. Points d'amélioration

1. 🔴 **Déploiement bloqué** — les corrections locales n'ont pas été poussées sur GitHub. La version live est toujours la maquette.
2. 🔴 **Zéro indexation** — tant que le bon titre n'est pas en production, le site n'a aucun signal de qualité pour Google.
3. ⚠️ **`article-speedboat.html` absent du sitemap** — un article n'est pas déclaré à Google.
4. ⚠️ **10 articles sans meta description** — Google génère des extraits automatiques, souvent moins pertinents.
5. ⚠️ **H1 sans mot-clé cible** — le H1 "Encore un consultant ? Non." est fort en conversion mais muet pour le SEO.

---

## Top 3 recommandations pour la semaine suivante

### 1. 🚨 Pousser le commit sur GitHub immédiatement
Les fichiers locaux sont prêts. Un `git add . && git commit -m "fix: titre SEO, canonical, articles"` suivi d'un `git push` déclenche automatiquement le redéploiement sur Cloudflare Pages. Vérifier ensuite en live que `<title>` affiche bien "Conseil Produit PME/PMI — Intelligence Produit | Lyon".

### 2. Ajouter `article-speedboat` au sitemap + demander l'indexation dans Search Console
Ajouter l'URL manquante dans `sitemap.xml` :
```xml
<url>
  <loc>https://intelligenceproduit.com/article-speedboat</loc>
  <changefreq>monthly</changefreq>
  <priority>0.7</priority>
</url>
```
Une fois déployé : Search Console → Sitemaps → soumettre `sitemap.xml` → inspecter et demander l'indexation pour la homepage et les 3 articles principaux.

### 3. Ajouter les meta descriptions manquantes sur les 10 articles
Priorité aux articles à fort potentiel de trafic :
- `article-diagnostic-360` ✅ déjà fait
- `article-5-pourquoi` — ajouter : *"La méthode des 5 Pourquoi pour remonter à la cause racine d'un problème produit en PME, sans s'arrêter au premier symptôme."*
- `article-chaine-valeur-porter` — ajouter : *"Comment appliquer la chaîne de valeur de Porter au diagnostic d'un produit en difficulté dans une PME ou PMI."*
- `article-diagnostic-combine` — ajouter : *"Porter, Ishikawa, AMDEC, 5 Pourquoi : comment combiner ces quatre outils pour un diagnostic produit complet."*

---

*Rapport généré automatiquement par l'audit SEO hebdomadaire Intelligence Produit — 3 août 2026.*
