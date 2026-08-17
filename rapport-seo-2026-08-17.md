# Rapport SEO hebdomadaire — intelligenceproduit.com
**Date de l'audit :** 17 août 2026  
**Audité par :** Intelligence Produit SEO Bot (tâche planifiée)

---

## Résumé exécutif

| | |
|---|---|
| **Score global SEO** | 🔴 **Faible** |
| **Évolution** | Premier audit de référence — pas de comparaison disponible |
| **Problème critique détecté** | La version déployée du site affiche "Maquette home (style réel)" dans le titre — une version de maquette/test est en production au lieu de la version finale |

Le site n'apparaît dans **aucun résultat Google** pour les mots-clés cibles. La cause principale probable est la combinaison de deux problèmes : un titre de page incorrect en production (contenant le mot "Maquette") et potentiellement une autorité de domaine encore trop faible pour les requêtes compétitives. L'indexation doit être vérifiée en priorité absolue.

---

## Indexation

| Indicateur | Résultat |
|---|---|
| Pages indexées (`site:intelligenceproduit.com`) | **0** — aucun résultat retourné ⚠️ |
| Sitemap accessible | ✅ Oui — https://intelligenceproduit.com/sitemap.xml |
| Nombre d'URLs dans le sitemap | **19 URLs** (5 pages principales + 13 articles + 1 ressource) |
| Problème www vs apex | Non détecté — le sitemap utilise uniquement `https://intelligenceproduit.com/` |

**Interprétation :** Le fait que `site:intelligenceproduit.com` ne retourne aucun résultat peut signifier (a) que Google n'a pas encore indexé le site, ou (b) que l'exploration est bloquée. Cette vérification via l'opérateur `site:` n'est pas toujours 100% fiable — il est recommandé de vérifier directement dans Google Search Console. Si Google Search Console confirme une couverture d'indexation nulle ou très basse, l'action est urgente.

---

## Titre de la page déployée — Problème critique

**Titre attendu (fichier local index.html) :**  
`Conseil Produit PME/PMI — Intelligence Produit | Lyon` ✅

**Titre constaté sur le site en production (https://intelligenceproduit.com/) :**  
`Intelligence Produit — Maquette home (style réel)` ❌

Ce titre indique que la version déployée sur Cloudflare Pages n'est **pas** la version du fichier `index.html` local. Une ancienne version de maquette semble être en production. C'est un problème critique : Google indexe ce titre erroné, ce qui signale au moteur de recherche que la page est une maquette/prototype, pas un site professionnel en activité.

**Action immédiate requise :** Vérifier le repo GitHub AltaAteliers/intelligence-produit et redéployer depuis la bonne branche.

---

## Mots-clés et positions

La recherche sur chacun des mots-clés cibles n'a retourné **aucune apparition de intelligenceproduit.com**. L'ensemble du tableau ci-dessous reflète une absence totale de visibilité organique au moment de l'audit.

| Mot-clé | Position estimée | URL positionnée | Notes |
|---------|-----------------|-----------------|-------|
| conseil produit PME | Non classé | — | Concurrents : Katalyse, Bpifrance, GAYA Conseil |
| coach produit PME PMI | Non classé | — | Résultats dominés par coaches dirigeants (pas "produit") |
| consultant product management PME | Non classé | — | Résultats en anglais / Suisse dominants |
| management produit PME Lyon | Non classé | — | Dominé par formations universitaires Lyon 1 & 2 |
| coach en management produit | Non classé | — | Opportunité : terme peu concurrentiel |
| diagnostic produit PME | Non classé | — | Dominé par NOTA-PME (Infogreffe), non directement concurrent |
| diagnostic 360 produit industriel | Non recherché | — | À tester — probablement faible concurrence |
| pourquoi mon produit ne se vend pas PME | Non classé | — | Requête conversationnelle — bonne cible pour article |
| product manager PME externalisé | Non classé | — | Quelques résultats suisses (lesdigivores.ch) |
| accompagnement lancement produit PME France | Non classé | — | Dominé par programmes gouvernementaux (Bpifrance, France 2030) |
| redéfinir produit industriel PME | Non recherché | — | À tester — probablement très faible concurrence |
| consultant produit Lyon PME | Non classé | — | ~8 cabinets concurrents visibles (KSTN, Egnoka, MD Consulting…) |
| intelligence produit PME | Non classé | — | Terme ambigu — Google le comprend comme "intelligence économique" ou "IA" |

---

## Analyse on-page (fichier local vs déployé)

### Fichier local (`index.html`) — ce qui devrait être en ligne

| Élément | Statut | Valeur |
|---------|--------|--------|
| `<title>` | ✅ Correct | `Conseil Produit PME/PMI — Intelligence Produit \| Lyon` |
| `<meta name="description">` | ✅ Conforme | "Votre produit ne se vend pas ? Faites appel à un entrepreneur et coach en management produit…" |
| `<link rel="canonical">` | ✅ Correct | `https://intelligenceproduit.com/` |
| `<meta property="og:url">` | ✅ Correct | `https://intelligenceproduit.com/` |
| `<meta property="og:title">` | ✅ Correct | Identique au `<title>` |
| `google-site-verification` | ✅ Présent | Code de vérification présent |
| JSON-LD `ProfessionalService` | ✅ Présent | Avec adresse, fondateur, areaServed:FR |
| `<h1>` | ⚠️ Sous-optimal | "Encore un consultant ? Non." — accrocheur mais aucun mot-clé SEO |
| `<h2>` | ⚠️ Unique | Un seul H2 : "Un problème produit précis en tête ?" |

### Site déployé — ce qui est réellement en ligne

| Élément | Statut | Problème |
|---------|--------|---------|
| `<title>` | 🔴 Critique | "Intelligence Produit — Maquette home (style réel)" |
| Reste des balises | Non vérifiable | La page déployée semble être une version différente du fichier local |

---

## Points forts

- **Technique locale solide :** le fichier `index.html` local est bien structuré — canonical, og:url, og:title, meta description, JSON-LD ProfessionalService, google-site-verification : tout est en place.
- **Sitemap complet :** 19 URLs organisées avec des priorités cohérentes ; le sitemap est accessible et bien formé.
- **Contenu éditorial existant :** 13 articles déjà présents dans le sitemap (diagnostic 360°, objets frontières, chaîne de valeur Porter, Ishikawa, AMDEC, etc.) — bon capital pour le SEO sémantique une fois indexés.
- **Positionnement différenciant :** l'angle "entrepreneur vs cabinet" est distinctif et peut générer des clics si la page arrive à se positionner.
- **Aucun problème www/apex** détecté : toutes les URLs du sitemap utilisent le domaine apex.

## Points d'amélioration

- 🔴 **[CRITIQUE] Version déployée ≠ fichier local :** Le titre "Maquette home" en production est catastrophique pour l'image professionnelle et l'indexation.
- 🔴 **Indexation incertaine :** Aucune page visible via `site:intelligenceproduit.com` — à confirmer dans Google Search Console.
- ⚠️ **H1 sans mots-clés :** "Encore un consultant ? Non." est un headline marketing, pas un signal SEO. Il manque un H1 ou une balise secondaire portant "conseil produit PME" ou "management produit PME".
- ⚠️ **Un seul H2 :** La structure de contenu est trop plate — les sections de la page ne sont pas balisées en H2/H3, ce qui prive Google de signaux de structure sémantique.
- ⚠️ **Terme "intelligence produit PME" ambigu :** Google l'interprète comme "intelligence économique" ou "intelligence artificielle" — le nom de marque est peu lisible pour les moteurs sur ce segment.
- ⚠️ **Aucune page de service dédiée par offre :** Les mots-clés longue traîne ("diagnostic 360 produit industriel", "accompagnement lancement produit PME") nécessitent des pages dédiées, pas seulement des mentions dans la page d'accueil.

---

## Top 3 recommandations pour la semaine suivante

### 1. 🔴 Redéployer la bonne version du site (priorité absolue)

Vérifier le repo GitHub `AltaAteliers/intelligence-produit` — la branche déployée sur Cloudflare Pages n'est pas la bonne. Le fichier `index.html` en production affiche "Maquette home (style réel)" au lieu du titre SEO correct. **Cette seule correction est la plus impactante de toutes.**  
→ Vérifier quelle branche est connectée à Cloudflare Pages et pousser le bon `index.html`.

### 2. Vérifier l'indexation dans Google Search Console

Se connecter à Search Console et vérifier :
- Combien de pages sont "Valides" vs "Exclues"
- Si le sitemap a été soumis et traité
- Si des erreurs de crawl sont signalées
- Demander une indexation manuelle via "Inspecter l'URL" pour la homepage

### 3. Ajouter les mots-clés cibles dans la structure H1/H2 de la homepage

Sans toucher au texte accrocheur, ajouter un sous-titre ou un H2 visible portant les mots-clés principaux, par exemple :
> **Conseil produit pour PME et PMI** — [phrase accrocheur existante]

Et restructurer les sections de la page (Positionnement, Diagnostic, Terrain…) avec des balises `<h2>` pour signaler la structure sémantique à Google.

---

*Prochain audit prévu : semaine du 24 août 2026*
