# Rapport SEO Hebdomadaire — intelligenceproduit.com
**Date de l'audit :** 31 juillet 2026

---

## Résumé exécutif

| Indicateur | Valeur |
|------------|--------|
| Score global SEO | 🔴 Faible |
| Pages indexées Google | 0 (aucune) |
| Sitemap accessible | ✅ Oui |
| Positionnement mots-clés | Non détecté |
| Évolution vs audit précédent | Premier audit de référence |

**Problème critique identifié :** Le titre affiché en production est `"Intelligence Produit — Maquette home (style réel)"` — le fichier index.html local a le bon titre, mais **la version déployée sur Cloudflare Pages ne correspond pas aux fichiers locaux**. C'est la cause principale de la non-indexation et de l'absence de positionnement.

---

## 1. Indexation

### Résultats `site:intelligenceproduit.com`
- **Pages indexées : 0**
- La recherche `site:intelligenceproduit.com` ne retourne aucun résultat. Google n'a pas (encore) indexé le site, ou l'a désindexé.
- Aucun problème de canonicalisation `www` vs apex détecté (le site redirige correctement vers `https://intelligenceproduit.com/`).

### Sitemap
- **Accessible :** ✅ `https://intelligenceproduit.com/sitemap.xml` répond (contenu XML binaire reçu).
- URLs présentes dans le sitemap : non lisibles en clair depuis l'audit automatisé — à vérifier manuellement dans Google Search Console.

### Hypothèse sur la non-indexation
Deux causes probables, cumulables :
1. **Le site est récent** et Google n'a pas encore crawlé et indexé les pages.
2. **La version live est une version de maquette** (titre "Maquette home (style réel)") — si cette version a été déployée tôt, Google a peut-être crawlé une page incomplète ou avec un signal de qualité faible.

---

## 2. Mots-clés et positions

Aucun mot-clé testé ne fait apparaître intelligenceproduit.com dans les résultats. Voici l'état de chaque groupe :

| Mot-clé | Position estimée | URL positionnée | Évolution | Notes |
|---------|-----------------|-----------------|-----------|-------|
| conseil produit PME | Non classé | — | Nouveau | Concurrents : eiphedeix, advyse, systemproject, katalyse |
| coach produit PME PMI | Non classé | — | Nouveau | Concurrents : audere.fr, ffcpro.org, katalyse |
| consultant product management PME | Non classé | — | Nouveau | Concurrents : thiga, wefiit, sortlist |
| management produit PME Lyon | Non classé | — | Nouveau | Concurrents : sortlist.fr, systemproject.fr, mdupreconsulting |
| coach en management produit | Non classé | — | Nouveau | — |
| diagnostic produit PME | Non classé | — | Nouveau | Résultats dominés par BPIFrance (financement) |
| diagnostic 360 produit industriel | Non classé | — | Nouveau | Niche peu couverte — opportunité |
| pourquoi mon produit ne se vend pas PME | Non classé | — | Nouveau | Résultats forum/blog — opportunité article |
| product manager PME externalisé | Non classé | — | Nouveau | — |
| accompagnement lancement produit PME France | Non classé | — | Nouveau | — |
| redéfinir produit industriel PME | Non classé | — | Nouveau | — |
| consultant produit Lyon PME | Non classé | — | Nouveau | Concurrents : adrixe-conseil, alkemys, systemproject |
| intelligence produit PME | Non classé | — | Nouveau | — |

**Observation :** Plusieurs mots-clés longue traîne (notamment "diagnostic 360 produit industriel" et "pourquoi mon produit ne se vend pas PME") sont peu ou pas couverts par des concurrents directs. Ce sont des opportunités de positionnement rapide dès que le site sera indexé.

---

## 3. Analyse on-page

### Homepage — comparaison live vs fichier local

| Élément | Version live (déployée) | Fichier local index.html | Statut |
|---------|------------------------|--------------------------|--------|
| `<title>` | "Intelligence Produit — Maquette home (style réel)" | "Conseil Produit PME/PMI — Intelligence Produit \| Lyon" | 🔴 **CRITIQUE** — maquette en prod |
| `<meta name="description">` | Non visible | ✅ Conforme au texte attendu | ⚠️ À vérifier en live |
| `<link rel="canonical">` | Non présent | **Absent** | 🔴 **MANQUANT** dans les deux |
| `og:url` | Non visible | ✅ `https://intelligenceproduit.com/` | ⚠️ À vérifier en live |
| `og:title` | Non visible | ✅ "Conseil Produit PME/PMI — Intelligence Produit \| Lyon" | ⚠️ À vérifier en live |
| Google Site Verification | Non visible | ✅ Présent (sFqfrB0wOUs0E…) | ⚠️ À vérifier en live |
| JSON-LD ProfessionalService | Non visible | ✅ Présent et complet | ⚠️ À vérifier en live |
| H1 | "Encore un consultant ? Non." | Idem | ⚠️ Aucun mot-clé cible dans le H1 |
| H2 | "Un problème produit précis en tête ?" | Idem | ⚠️ Pas de mot-clé |
| H3 | "Un diagnostic qui remonte à la vraie cause", "Le terrain avant tout", etc. | Idem | ℹ️ Pertinents mais non optimisés |

### Problème majeur : le H1 n'est pas optimisé

Le H1 "Encore un consultant ? Non." est accrocheur pour la conversion, mais Google s'en sert comme signal de pertinence thématique. Il ne contient aucun des mots-clés cibles (conseil produit, PME, Lyon, diagnostic).

---

## 4. Points forts

- ✅ **Sitemap présent** et accessible
- ✅ **JSON-LD ProfessionalService** bien structuré (adresse, fondateur, périmètre)
- ✅ **Google Site Verification** en place — Search Console peut être utilisée
- ✅ **Meta description** conforme dans le fichier local — claire, avec les mots-clés principaux
- ✅ **og:url et og:title** corrects dans le fichier local
- ✅ **Niche peu encombrée** : "diagnostic 360 produit industriel PME" et "pourquoi mon produit ne se vend pas PME" ont une faible concurrence directe
- ✅ **Articles publiés** (diagnostic 360, objets frontières, design PME) — capital de contenu existant

---

## 5. Points d'amélioration

1. 🔴 **Version maquette en production** — le titre live ne correspond pas au fichier local. Déployer immédiatement.
2. 🔴 **Zéro indexation** — soumettre le sitemap dans Google Search Console, forcer l'inspection des URLs.
3. 🔴 **Balise canonical absente** — à ajouter dans tous les fichiers HTML.
4. ⚠️ **H1 sans mot-clé** — le H1 de la homepage ne signal pas le thème à Google.
5. ⚠️ **Articles non linkés dans le sitemap** — à vérifier : les 8+ articles HTML sont-ils dans le sitemap ?

---

## Top 3 recommandations pour la semaine suivante

### 1. 🚨 Déployer immédiatement la bonne version du site
Le fichier `index.html` local a le titre correct. Pousser le commit sur GitHub → Cloudflare Pages redéploie automatiquement. Vérifier ensuite en live que `<title>` est bien "Conseil Produit PME/PMI — Intelligence Produit | Lyon".

### 2. Ajouter la balise canonical sur toutes les pages
Insérer dans le `<head>` de chaque page HTML :
```html
<link rel="canonical" href="https://intelligenceproduit.com/[nom-de-la-page].html">
```
Pour la homepage :
```html
<link rel="canonical" href="https://intelligenceproduit.com/">
```
C'est une protection contre les doublons et un signal fort pour Google.

### 3. Forcer l'indexation via Google Search Console
Une fois le bon titre déployé :
- Ouvrir Search Console → Inspection d'URL → taper `https://intelligenceproduit.com/`
- Cliquer "Demander l'indexation"
- Faire de même pour les 3 articles principaux
- Vérifier que le sitemap est bien soumis (section Sitemaps)

---

*Rapport généré automatiquement par l'audit SEO hebdomadaire Intelligence Produit.*
