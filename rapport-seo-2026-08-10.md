# Rapport SEO hebdomadaire — intelligenceproduit.com
**Date :** 10 août 2026  
**Audité par :** Claude (automatisé)  
**URL :** https://intelligenceproduit.com/

---

## Résumé exécutif

| Critère | Statut |
|---|---|
| Score global SEO | **FAIBLE** ⚠️ |
| Évolution | Premier audit de référence |
| Problème critique détecté | **Oui — titre live non déployé** |

Le site est techniquement accessible et les fichiers locaux sont bien optimisés SEO. Mais **la version live du site affiche encore le titre de maquette "Intelligence Produit — Maquette home (style réel)"** — ce qui signifie que les fichiers locaux n'ont pas été déployés sur Cloudflare Pages. C'est probablement la principale raison pour laquelle le site n'apparaît pas dans les résultats Google.

---

## 1. Indexation

### `site:intelligenceproduit.com`
La recherche `site:intelligenceproduit.com` n'a retourné **aucun résultat** pour le domaine. Le site ne semble pas indexé par Google (ou son indexation est très récente et incomplète).

- **Cause probable :** Le titre live de la homepage est "Intelligence Produit — Maquette home (style réel)". Un titre contenant le mot "maquette" peut signaler à Google qu'il s'agit d'une page de développement/test, réduisant fortement la probabilité d'indexation.
- **Pas de problème de canonicalisation www vs apex détecté** (le site répond uniquement sur l'apex `intelligenceproduit.com`).

### Sitemap
- **Accessible :** Oui — https://intelligenceproduit.com/sitemap.xml
- **Nombre d'URLs dans le sitemap :** 19 URLs (6 pages principales + 13 articles)
- **Note :** Les URLs du sitemap n'ont pas d'extension `.html` (ex : `/qui-suis-je`), mais les fichiers locaux ont l'extension `.html`. Vérifier que Cloudflare redirige bien `/qui-suis-je` → `/qui-suis-je.html` ou que les URLs servent sans extension.

---

## 2. Mots-clés et positions

> **Note :** intelligenceproduit.com n'apparaît dans **aucun** des résultats pour les mots-clés testés. La colonne "Évolution" n'est pas applicable pour ce premier audit.

| Mot-clé | Position estimée | URL positionnée | Notes |
|---|---|---|---|
| conseil produit PME | Non visible | — | BPI France, Katalyse, Gaya Conseil en tête |
| coach produit PME PMI | Non visible | — | LinkedIn, coaching RH, audere.fr en tête |
| consultant product management PME | Non visible | — | Résultats en anglais, lesdigivores.ch |
| management produit PME Lyon | Non visible | — | ISFA Lyon 1, masters universitaires |
| coach en management produit | Non visible | — | — |
| diagnostic produit PME | Non visible | — | NOTA-PME (BPI), diagnostics financiers |
| diagnostic 360 produit industriel | Non visible | — | CCI Grand Est, Gaya Conseil, Noveliah |
| pourquoi mon produit ne se vend pas PME | Non visible | — | LiveMentor, pierrebertucat.com |
| product manager PME externalisé | Non visible | — | lesdigivores.ch, yieldstudio.fr |
| accompagnement lancement produit PME France | Non visible | — | Résultats institutionnels (BPI, France 2030) |
| redéfinir produit industriel PME | Non visible | — | agileforce.fr, gayaconseil.com |
| consultant produit Lyon PME | Non visible | — | KSTN, Egnoka, Alkemys, Mdupréconsulting |
| intelligence produit PME | Non visible | — | IA PME Conseil (IA), résultats hors sujet |
| diagnostic 360° PME | Non visible | — | CCI Nancy, Gaya Conseil, Noveliah |

**Observation :** La requête "intelligence produit PME" est détournée vers des résultats sur l'intelligence artificielle pour PME — ce qui peut nuire à la visibilité de la marque sur ce terme générique.

---

## 3. Analyse on-page

### Comparatif local vs live

| Balise | Fichier local (index.html) | Live (intelligenceproduit.com) | Statut |
|---|---|---|---|
| `<title>` | Conseil Produit PME/PMI — Intelligence Produit \| Lyon | **Intelligence Produit — Maquette home (style réel)** | ❌ CRITIQUE |
| `<link rel="canonical">` | `https://intelligenceproduit.com/` | Non vérifié (live) | ✅ Local OK |
| `og:url` | `https://intelligenceproduit.com/` | Non vérifié (live) | ✅ Local OK |
| `og:title` | Conseil Produit PME/PMI — Intelligence Produit \| Lyon | Non vérifié (live) | ✅ Local OK |
| Meta description | Présente, conforme | Non vérifié (live) | ✅ Local OK |
| google-site-verification | Présente | Non vérifié (live) | ✅ Local OK |
| JSON-LD ProfessionalService | Présent, complet | Non vérifié (live) | ✅ Local OK |
| `<h1>` | "Encore un consultant ? Non." | — | ⚠️ Faible en mots-clés |

### Détail JSON-LD (local)
- Type : `ProfessionalService` ✅
- Founder : Grégoire Gérard + lien LinkedIn ✅
- Adresse : Tassin-la-Demi-Lune 69160 ✅
- `areaServed` : FR ✅
- `sameAs` LinkedIn ✅

### H1 et structure de contenu
Le H1 est "Encore un consultant ? Non." — accrocheur pour un visiteur humain, mais pauvre en mots-clés SEO. Aucune des expressions cibles (conseil produit PME, diagnostic 360, Lyon) n'apparaît dans le H1. Le terme "Conseil produit — PME & PMI" apparaît dans un `<div class="badge">` au-dessus du H1, ce qui ne compte pas pour Google.

---

## 4. Points forts

- **Structure locale très propre** : canonical, og:url, meta description, JSON-LD sont tous bien renseignés dans les fichiers locaux.
- **Sitemap présent** avec 19 URLs dont 13 articles — bonne surface de contenu.
- **Google Search Console vérifiée** (balise de vérification présente).
- **Contenu thématique pertinent** : les articles (diagnostic 360, Ishikawa, Porter, FMEA, objets frontières) couvrent exactement les requêtes de la cible.
- **Pas de problème de canonicalisation www/apex** apparent.

---

## 5. Points d'amélioration

1. **🔴 CRITIQUE — Déploiement non effectué** : Le live affiche le titre "Maquette home" — les fichiers locaux optimisés n'ont pas été pushés sur GitHub / déployés via Cloudflare Pages.
2. **🔴 Non-indexation** : Le site n'apparaît dans aucune recherche `site:` ni sur aucun mot-clé cible. Probablement dû au problème de titre ci-dessus.
3. **🟡 H1 non optimisé** : "Encore un consultant ? Non." ne contient aucun mot-clé cible. Idéalement : reformuler pour inclure "conseil produit PME" ou "diagnostic produit PME/PMI".
4. **🟡 URLs sitemap sans extension** : Les URLs du sitemap (`/qui-suis-je`, `/offres`) diffèrent des fichiers locaux (`qui-suis-je.html`). S'assurer que Cloudflare sert les pages sans extension ou configure des redirections.
5. **🟡 Term "intelligence produit"** capturé par les résultats IA : envisager d'optimiser sur des requêtes plus explicites comme "conseil produit PME Lyon" ou "diagnostic produit industriel".
6. **🟠 Pas de backlinks** détectés sur les recherches : à construire (LinkedIn, annuaires pros Lyon, presse spécialisée PME).

---

## Top 3 recommandations pour la semaine suivante

### 🔴 1. Déployer immédiatement sur Cloudflare Pages
Committer et pusher les fichiers locaux vers le repo GitHub `AltaAteliers/intelligence-produit`. Le déploiement automatique Cloudflare Pages corrigera le titre live et permettra à Google d'indexer les bonnes métadonnées. C'est l'action la plus urgente — tout le reste dépend de ça.

### 🟡 2. Optimiser le H1 de la homepage
Remplacer "Encore un consultant ? Non." par une formulation qui inclut les mots-clés cibles tout en restant percutante pour un visiteur humain. Exemple :
> "Votre produit PME/PMI mérite mieux qu'un cabinet classique."
> (ou : "Conseil produit terrain pour PME et PMI — pas du conseil de bureau.")

Le badge "Conseil produit — PME & PMI" pourrait être intégré directement dans ou sous le H1 pour renforcer le signal sémantique.

### 🟡 3. Soumettre le sitemap dans Google Search Console
Une fois le déploiement effectué, aller dans Google Search Console → Sitemaps → soumettre `https://intelligenceproduit.com/sitemap.xml`. Demander également l'indexation manuelle de la homepage via "Inspecter l'URL". Cela accélérera l'indexation des 19 URLs.

---

*Prochain audit prévu : semaine prochaine (automatisé)*
