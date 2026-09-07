# Rapport SEO hebdomadaire — intelligenceproduit.com
**Date de l'audit :** 31 août 2026
**Audité par :** Intelligence Produit SEO Bot (tâche planifiée)
**Audit précédent :** 24 août 2026

---

## Résumé exécutif

| | |
|---|---|
| **Score global SEO** | 🟡 **Moyen** |
| **Évolution vs 24 août** | **=** — aucun changement, aucune recommandation appliquée |
| **Balisage technique** | ✅ Toujours conforme |
| **Blocage principal** | Indexation toujours à zéro, aucune action Search Console confirmée |

Semaine blanche. Aucun des trois chantiers recommandés le 24 août n'a été engagé : pas de commit depuis `8455c8c`, fichiers locaux inchangés depuis le 31 juillet, sitemap identique, H1 identique. Le site reste techniquement propre et commercialement invisible.

**Une bonne nouvelle quand même :** en vérifiant le maillage interne cette semaine, j'ai constaté que Cloudflare Pages **redirige en 301** les URLs `.html` vers les URLs canoniques sans extension (`/qui-suis-je.html` → `/qui-suis-je`, `/index.html` → `/`). Le point signalé la semaine dernière comme un risque de contenu dupliqué n'en est donc pas un — c'est un simple saut de redirection supplémentaire. **Je corrige mon diagnostic du 24 août** : la recommandation n°2 passe de « ⚠️ important » à « optimisation mineure ».

Conséquence : il ne reste qu'un seul vrai blocage, et il est hors du site.

---

## Indexation

| Indicateur | Résultat | Évolution |
|---|---|---|
| Pages indexées (`site:intelligenceproduit.com`) | **0** — aucun résultat retourné | = |
| Sitemap accessible | ✅ Oui | = |
| URLs dans le sitemap | **19** (6 pages principales + 13 articles) | = |
| Problème www vs apex | Non détecté — apex uniquement | = |
| Redirections `.html` → URL propre | ✅ **301 en place** (constat nouveau) | ↑ correction |
| `article-speedboat` dans le sitemap | ❌ Toujours absent (signalé le 3 août) | = |

**Note méthodologique inchangée :** l'opérateur `site:` de l'API de recherche utilisée n'est pas fiable — il renvoie des résultats sans rapport (SITE Intelligence Group, intelligence.gov). Un résultat vide ne prouve pas formellement une indexation nulle. Seule Search Console tranche. C'est la quatrième semaine consécutive que cette vérification est reportée.

**Signal indirect :** une requête de marque (`intelligenceproduit.com Grégoire Gérard conseil produit PME`) fait toujours remonter le **profil LinkedIn** de Greg, jamais le site. Si le domaine était indexé, une requête contenant le nom de domaine exact devrait le faire apparaître. C'est un indice fort — pas une preuve — que l'indexation est bien nulle.

---

## Mots-clés et positions

| Mot-clé | Position estimée | URL positionnée | Évolution | Notes |
|---------|-----------------|-----------------|-----------|-------|
| conseil produit PME | Non classé | — | = | Bpifrance, GAYA Conseil, EVOYKO, Pro PME |
| coach produit PME PMI | Non classé | — | = | SERP 100 % coaching de dirigeants — aucun acteur produit |
| consultant product management PME | Non classé | — | = | SERP anglophone (PMX Group, Get Product People, Procore) |
| management produit PME Lyon | Non classé | — | = | SERP entièrement académique (ISFA, Lyon 2, BTS GPME) |
| coach en management produit | Non classé | — | = | Thiga, Opilus — cible tech/startup, pas PMI |
| diagnostic produit PME | Non classé | — | = | NOTA-PME (financier) domine ; Morisseau, Man&O, MACS |
| diagnostic 360 produit industriel | Non classé | — | = | ⚠️ GAYA Conseil toujours n°2 avec sa page dédiée « Diagnostic 360° pour PME industrielles » |
| pourquoi mon produit ne se vend pas PME | Non classé | — | = | SERP faible (forums, e-commerce, blogs perso) — **opportunité la plus accessible** |
| product manager PME externalisé | Non classé | — | = | Les DIGIVORES (Suisse), Yield Studio — **aucun acteur français industriel** |
| accompagnement lancement produit PME France | Non classé | — | = | Bpifrance / France 2030 monopolisent — intention publique, pas commerciale |
| redéfinir produit industriel PME | Non classé | — | = | CPME, ERP Open-Prod — pas de concurrent conseil |
| consultant produit Lyon PME | Non classé | — | = | KSTN, Egnoka, MD Consulting, Otago, System:Project |
| intelligence produit PME | Non classé | — | = | Google lit « intelligence économique » / « intelligence artificielle » |

**13 mots-clés testés, 13 non classés.** Identique aux quatre audits précédents.

### Lecture concurrentielle de la semaine

Trois SERP se démarquent par leur faiblesse, dans l'ordre d'accessibilité :

1. **« pourquoi mon produit ne se vend pas »** — occupée par des forums, des blogs e-commerce et des articles génériques. Aucune page de conseil B2B industriel. L'article `article-diagnostic-360.html` traite exactement ce sujet et porte déjà le titre « Pourquoi votre produit ne se vend pas — méthode à 360° ».
2. **« product manager PME externalisé »** — le seul acteur positionné (Les DIGIVORES) est suisse et cible le numérique. Le créneau « PM externalisé pour PMI industrielle » est vide en France.
3. **« redéfinir produit industriel PME »** — SERP occupée par des éditeurs d'ERP et des rapports institutionnels. Aucune offre de conseil.

À l'inverse, **« conseil produit PME »** et **« consultant produit Lyon PME »** sont saturées de cabinets établis. Ce sont les mots-clés du titre actuel, et ce sont les plus durs à gagner. Le positionnement SEO du site vise aujourd'hui les requêtes les plus concurrentielles et ignore les trois créneaux vides ci-dessus.

---

## Analyse on-page — page d'accueil (version LIVE)

| Élément | Statut | Valeur constatée en production |
|---------|--------|-------------------------------|
| `<title>` | ✅ Conforme | `Conseil Produit PME/PMI — Intelligence Produit \| Lyon` |
| `<meta name="description">` | ✅ Conforme | Texte attendu, mot pour mot |
| `<link rel="canonical">` | ✅ Correct | `https://intelligenceproduit.com/` |
| `og:url` | ✅ Correct | `https://intelligenceproduit.com/` |
| `og:title` / `og:description` / `og:image` / `og:type` | ✅ Présents | Image `hero-greg.jpg` |
| `twitter:card` | ✅ Présent | `summary_large_image` |
| `google-site-verification` | ✅ Présent | `sFqfrB0wOUs0E_mQCDwT9U2cfhQq-4rxvGYKXAFKelo` |
| JSON-LD | ✅ Présent | `ProfessionalService` + `Person` (fondateur) + `PostalAddress` (Tassin) |
| `<h1>` | ⚠️ Sans mot-clé | « Encore un consultant ? Non. » — inchangé |
| Hiérarchie Hn | ⚠️ Cassée | 1 H1 → 4 H3 → 1 H2 → 3 H4. Aucun H2 avant le premier H3. |

### Détail de la hiérarchie Hn (inchangé depuis le 24 août)

```
H1  Encore un consultant ? Non.
H3  Un diagnostic qui remonte à la vraie cause     ← devrait être sous un H2 "Positionnement"
H3  Le terrain avant tout
H3  Pas de blabla
H3  Kaskadia                                        ← devrait être sous un H2 "Outils"
H2  Un problème produit précis en tête ?            ← seul H2, en bas de page
H4  ×3 (titres d'articles)                          ← devraient être sous un H2 "Articles"
```

Les intitulés de section existent bien visuellement (« Positionnement », « Outils en libre accès », « Derniers articles ») mais ne sont pas balisés en H2. Google lit donc une page à un seul niveau de sens.

### Autres pages
`qui-suis-je` reste la page la mieux optimisée du site : titre porteur (« Entrepreneur & Coach Produit PME »), meta description factuelle avec noms d'entreprises (Altran, Holi, SIREM, Kaskadia), 4 H2 thématiques, parcours détaillé, lien LinkedIn sortant. Canonical propre.

---

## Points forts

- **Balisage technique complet et sans défaut** : canonical, og:*, twitter:card, JSON-LD `ProfessionalService` + `Person` + `PostalAddress`, google-site-verification, robots.txt avec directive Sitemap.
- **Redirections 301 `.html` → URL canonique en place** — le risque de duplication signalé la semaine dernière n'existe pas. Cloudflare Pages fait le travail.
- **Aucun problème www/apex.**
- **14 articles de fond** couvrant un champ sémantique cohérent (diagnostic 360°, Ishikawa, AMDEC, 5 pourquoi, chaîne de valeur Porter, objets frontières, sales book).
- **Page `qui-suis-je` de très bonne facture**, prête à capter les requêtes de marque et de personne.

## Points d'amélioration

- 🔴 **Indexation toujours nulle et toujours non vérifiée.** Quatrième semaine. Tant que Search Console n'est pas consultée, chaque audit répétera le même constat sans pouvoir l'expliquer.
- 🔴 **Zéro backlink identifié.** Le LinkedIn de Greg capte l'autorité que le site devrait capter.
- 🔴 **Aucune page de service dédiée.** Le site n'a que des pages génériques (`offres`) et des articles. Les trois créneaux SEO vides identifiés ci-dessus n'ont aucune page cible.
- ⚠️ **H1 sans mot-clé** et **hiérarchie Hn cassée** (aucun H2 structurant).
- ⚠️ **`article-speedboat` absent du sitemap** — quatrième semaine de signalement.
- ℹ️ **Maillage interne en `.html`** — déclassé en optimisation mineure grâce aux 301, mais fait perdre un saut de crawl sur chaque lien.

---

## Top 3 recommandations pour la semaine suivante

### 1. 🔴 Ouvrir Google Search Console — 15 minutes, quatrième relance

La balise de vérification est en place depuis un mois. Rien d'autre n'a besoin d'être fait techniquement. La seule action manquante est humaine :

- Ouvrir [search.google.com/search-console](https://search.google.com/search-console)
- Soumettre `https://intelligenceproduit.com/sitemap.xml` (Index → Sitemaps)
- Inspecter l'URL `https://intelligenceproduit.com/` → **Demander une indexation**
- Répéter pour `/qui-suis-je`, `/offres`, `/article-diagnostic-360`
- Relever dans « Pages » le nombre de pages **Valides** vs **Non indexées**, et la raison affichée

**Ce qu'on cherche à savoir :** si Google a crawlé le site et l'a écarté (et pourquoi), ou s'il ne l'a jamais découvert. Ce sont deux problèmes opposés qui appellent deux réponses opposées. Sans cette information, tout le reste est de la spéculation.

Si un rapport apparaît, en copier le résumé dans le dossier — l'audit de la semaine prochaine pourra enfin comparer autre chose que des zéros.

### 2. Créer la page `/pourquoi-mon-produit-ne-se-vend-pas`

Changement de cible par rapport à la semaine dernière (où je recommandais la page « Diagnostic 360° »). Raison : sur `diagnostic 360 produit industriel`, GAYA Conseil est solidement installé avec exactement ce format de page. Sur `pourquoi mon produit ne se vend pas`, la SERP est composée de forums LiveMentor, de blogs e-commerce et d'articles génériques — **aucun concurrent B2B industriel**. C'est la porte d'entrée la moins défendue du portefeuille, et c'est aussi la formulation exacte de la douleur du client cible.

Le matériau existe déjà : `article-diagnostic-360.html` porte littéralement ce titre. Il s'agit de le transformer en page de service :

- H1 : « Pourquoi votre produit ne se vend pas ? »
- H2 structurants : les 6 causes possibles (produit, prix, distribution, message, timing, organisation)
- Un H2 par cause, avec un exemple industriel concret
- H2 final : « Le diagnostic 360° Intelligence Produit » → méthode, livrables, durée, CTA Calendly
- Ajouter au sitemap, lier depuis la home et depuis `offres`

Bénéfice secondaire : cette page répond à une question, donc elle est citable par les moteurs de réponse (ChatGPT, Perplexity, AI Overviews) — un canal où l'autorité de domaine pèse beaucoup moins qu'en SEO classique. Pour un site neuf sans backlink, c'est le levier le plus rapide.

### 3. Réparer la hiérarchie Hn de la homepage — 20 minutes

Trois modifications dans `index.html`, sans toucher au design (les intitulés existent déjà en texte, il suffit de les baliser) :

| Section | Aujourd'hui | À faire |
|---|---|---|
| Positionnement | texte nu + 3 H3 | `<h2>Conseil produit pour PME et PMI industrielles</h2>` avant les H3 |
| Outils | texte nu + H3 Kaskadia | `<h2>Outils produit en libre accès</h2>` |
| Articles | texte nu + 3 H4 | `<h2>Ressources pour dirigeants de PME/PMI</h2>` puis passer les H4 en H3 |

Et remplacer le H1 « Encore un consultant ? Non. » par une formulation qui garde l'accroche tout en portant le mot-clé — par exemple **« Encore un consultant produit ? Non. Un entrepreneur. »** L'accroche survit, le mot-clé entre.

Dans la même passe : ajouter `article-speedboat` au sitemap (une ligne).

---

## Suivi des recommandations précédentes

| Recommandation (24 août) | Statut |
|---|---|
| 1. Confirmer l'indexation dans Search Console | ❌ Non fait — **4ᵉ report** |
| 2. Aligner le maillage interne sur les canonicals | ❌ Non fait — **déclassé** : les 301 rendent le problème mineur |
| 3. Créer une page dédiée « Diagnostic 360° produit industriel » | ❌ Non fait — **remplacée** par une cible moins concurrentielle (reco n°2 ci-dessus) |
| (17 août) Ajouter les mots-clés dans H1/H2 | ❌ Non fait — reportée en reco n°3 |
| (3 août) Ajouter `article-speedboat` au sitemap | ❌ Non fait — 4ᵉ report |

**Constat de méthode :** cinq audits, une seule recommandation appliquée (le redéploiement du 24 août). Les recommandations s'empilent plus vite qu'elles ne sont traitées. La reco n°1 conditionne tout le reste et coûte 15 minutes — si une seule chose doit être faite cette semaine, c'est celle-là.

---

## Sources consultées

- [GAYA Conseil — Diagnostic 360° pour PME industrielles](https://gayaconseil.com/diagnostic-360/)
- [GAYA Conseil — Conseil PME](https://gayaconseil.com/conseil-pme/)
- [KSTN — Cabinet de conseil stratégie PME Lyon](https://www.kstn.fr/cabinet-conseil-strategie-lyon.html)
- [Egnoka — Conseil stratégique PME Lyon](https://www.egnoka.fr/nos-bureaux/conseil-strategique-pme-lyon/)
- [Les DIGIVORES — Product Management externalisé pour PME](https://www.lesdigivores.ch/product-management-externalise-une-solution-agile-pour-les-pme-de-larc-lemanique/)
- [Opilus — Poste et mission de coach produit](https://www.opilus.fr/poste-mission-coach-produit/)
- [Profil LinkedIn Greg Gerard — Intelligence Produit](https://www.linkedin.com/in/gregoiregerard/)

---

*Prochain audit prévu : semaine du 7 septembre 2026*
