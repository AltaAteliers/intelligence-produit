# Rapport SEO hebdomadaire — intelligenceproduit.com
**Date de l'audit :** 7 septembre 2026
**Audité par :** Intelligence Produit SEO Bot (tâche planifiée)
**Audit précédent :** 31 août 2026

---

## Résumé exécutif

| | |
|---|---|
| **Score global SEO** | 🟡 **Moyen** |
| **Évolution vs 31 août** | **=** — aucun changement, aucune recommandation appliquée |
| **Balisage technique** | ✅ Toujours conforme |
| **Blocage principal** | Indexation toujours à zéro, Search Console toujours non consultée (5ᵉ semaine) |

Deuxième semaine blanche consécutive. Aucun commit depuis `8455c8c`, fichiers locaux inchangés depuis le 31 juillet, sitemap identique, H1 identique, hiérarchie Hn identique. Les trois recommandations du 31 août n'ont pas été engagées.

**Deux constats nouveaux cette semaine**, issus d'une inspection du corpus d'articles (jamais auditée jusqu'ici) :

1. **Le schema `Article` n'existe que sur 3 des 14 articles** — précisément les 3 mis en avant sur la homepage. Les 11 autres n'ont aucun balisage structuré.
2. **Le maillage interne entre articles est nul** : aucun des 14 articles ne pointe vers un autre article. Le corpus est une collection de feuilles isolées, pas un cluster thématique.

Ces deux points sont importants parce que le site n'a aucun backlink : le maillage interne est le seul levier d'autorité disponible, et il n'est pas utilisé.

---

## Indexation

| Indicateur | Résultat | Évolution |
|---|---|---|
| Pages indexées (`site:intelligenceproduit.com`) | **0** — aucun résultat retourné | = |
| Sitemap accessible | ✅ Oui (HTTP 200, `application/xml`) | = |
| URLs dans le sitemap | **19** (6 pages principales + 13 articles) | = |
| Problème www vs apex | Non détecté — apex uniquement dans toutes les SERP testées | = |
| Redirections `.html` → URL propre | ✅ 301 confirmées à nouveau (`/article-diagnostic-360.html` → `/article-diagnostic-360`) | = |
| `article-speedboat` dans le sitemap | ❌ Toujours absent (signalé le 3 août) | = — **5ᵉ report** |
| `robots.txt` | ✅ `Allow: /` + directive Sitemap + `Content-Signal: search=yes,ai-input=yes` | = |

**Note méthodologique inchangée :** l'opérateur `site:` de l'API de recherche utilisée n'est pas fiable — il renvoie des résultats sans rapport (SITE Intelligence Group, intelligence.gov, intelligence.com). Un résultat vide ne prouve pas formellement une indexation nulle. Seule Search Console tranche. C'est la cinquième semaine consécutive que cette vérification est reportée.

**Signal indirect (inchangé) :** la requête `"intelligenceproduit.com" Grégoire Gérard` fait remonter le profil LinkedIn de Greg en position 1, jamais le site — alors que la requête contient le nom de domaine exact entre guillemets. Indice fort, pas preuve, d'une indexation nulle.

**Note sur `www.intelligenceproduit.com` :** la vérification directe du sous-domaine `www` a été bloquée cette semaine par les restrictions de récupération d'URL de l'outil. Le constat « pas de problème www/apex » repose donc uniquement sur l'absence d'URL `www` dans les SERP testées, comme les semaines précédentes. À confirmer dans Search Console (qui affichera les deux propriétés si les deux sont servies).

---

## Mots-clés et positions

| Mot-clé | Position estimée | URL positionnée | Évolution | Notes |
|---------|-----------------|-----------------|-----------|-------|
| conseil produit PME | Non classé | — | = | outil-conseil-pme.fr, GAYA Conseil, EVOYKO, Pro PME, Advyse |
| coach produit PME PMI | Non classé | — | = | SERP 100 % coaching de dirigeants — toujours aucun acteur produit |
| consultant product management PME | Non classé | — | = | SERP anglophone (Procore, PMX Group, Get Product People, Productboard) |
| management produit PME Lyon | Non classé | — | = | SERP entièrement académique (ISFA, Lyon 1, Lyon 2, BTS GPME ESUP) |
| coach en management produit | Non classé | — | = | Thiga, Opilus, Devoteam — cible tech/startup, pas PMI |
| diagnostic produit PME | Non classé | — | = | NOTA-PME (financier) domine ; Morisseau, Man&O, MACS, Polynectar |
| diagnostic 360 produit industriel | Non classé | — | = | ⚠️ SERP qui **se densifie** : GAYA Conseil rejoint par ADRIA, XXL Stratégie, Coesor, KeyWe, Impulsion Conseil |
| pourquoi mon produit ne se vend pas PME | Non classé | — | = | SERP faible (forums LiveMentor, blogs e-commerce) — **opportunité la plus accessible** |
| product manager PME externalisé | Non classé | — | = | Les DIGIVORES (Suisse), Yield Studio / Yield Advisory — **toujours aucun acteur français industriel** |
| accompagnement lancement produit PME France | Non classé | — | = | Bpifrance / France 2030 / FEDER monopolisent — intention publique, pas commerciale |
| redéfinir produit industriel PME | Non classé | — | = | CPME, ERP Open-Prod, MagDesign — pas de concurrent conseil |
| consultant produit Lyon PME | Non classé | — | = | ODICEO, KSTN, Egnoka, Alkemys, MD Consulting, Otago, System:Project |
| intelligence produit PME | Non classé | — | = | Google lit « intelligence économique » / « intelligence artificielle » |

**13 mots-clés testés, 13 non classés.** Identique aux cinq audits précédents.

### Lecture concurrentielle de la semaine

**Alerte sur `diagnostic 360 produit industriel`.** La semaine dernière, GAYA Conseil était le seul concurrent sérieux. Cette semaine la SERP compte au moins **six** pages « Diagnostic 360° » dédiées (ADRIA pour l'agroalimentaire, XXL Stratégie, GAYA, Coesor, KeyWe, Impulsion Conseil). Ce mot-clé se ferme. La décision du 31 août de renoncer à cette cible au profit de « pourquoi mon produit ne se vend pas » se confirme comme le bon arbitrage — avec une semaine d'avance sur la fermeture du créneau.

Le classement des trois créneaux accessibles reste inchangé :

1. **« pourquoi mon produit ne se vend pas »** — forums, blogs e-commerce, articles génériques. Aucune page de conseil B2B industriel. L'article `article-diagnostic-360.html` porte déjà littéralement ce titre.
2. **« product manager PME externalisé »** — le seul acteur positionné est suisse et cible le numérique. Le créneau « PM externalisé pour PMI industrielle » reste vide en France.
3. **« redéfinir produit industriel PME »** — éditeurs d'ERP et rapports institutionnels. Aucune offre de conseil.

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
| `google-site-verification` | ✅ Présent (non supprimé) | `sFqfrB0wOUs0E_mQCDwT9U2cfhQq-4rxvGYKXAFKelo` |
| JSON-LD | ✅ Présent | `ProfessionalService` + `Person` (fondateur) + `PostalAddress` (Tassin) + `areaServed: FR` |
| `<h1>` | ⚠️ Sans mot-clé | « Encore un consultant ? Non. » — inchangé |
| Hiérarchie Hn | ⚠️ Cassée | 1 H1 → 4 H3 → 3 H4 → 1 H2. Aucun H2 avant le premier H3. |

### Détail de la hiérarchie Hn (inchangé depuis le 24 août)

```
H1  Encore un consultant ? Non.
H3  Un diagnostic qui remonte à la vraie cause     ← devrait être sous un H2 "Positionnement"
H3  Le terrain avant tout
H3  Pas de blabla
H3  Kaskadia                                        ← devrait être sous un H2 "Outils"
H4  ×3 (titres d'articles)                          ← devraient être sous un H2 "Articles"
H2  Un problème produit précis en tête ?            ← seul H2, en bas de page
```

Les intitulés de section existent bien visuellement (« Positionnement », « Outils en libre accès », « Derniers articles ») mais ne sont pas balisés en H2. Google lit donc une page à un seul niveau de sens.

### 🆕 Analyse du corpus d'articles (14 articles) — nouveau cette semaine

Premier audit du corpus lui-même, au-delà de la homepage.

| Contrôle | Résultat |
|---|---|
| Articles avec schema `Article` (auteur + éditeur + `inLanguage: fr`) | **3 / 14** — `article-diagnostic-360`, `article-design-pme`, `article-objets-frontieres` |
| Articles sans aucun JSON-LD | **11 / 14** |
| Articles avec un lien vers un autre article | **0 / 14** |
| Articles avec CTA Calendly | 14 / 14 ✅ |
| Articles avec canonical propre | 14 / 14 ✅ |
| Articles listés dans `ressources-demo` | 14 / 14 ✅ |
| Articles présents dans le sitemap | 13 / 14 (`article-speedboat` manquant) |

**Corrélation évidente :** les 3 articles balisés sont exactement les 3 mis en avant sur la homepage. Le schema a été ajouté au moment de leur mise en avant, puis jamais généralisé. Le schema existant est de bonne qualité (auteur avec `sameAs` LinkedIn, éditeur, URL canonique, langue) — il suffit de le dupliquer en changeant trois champs.

**Le maillage interne nul est le point le plus coûteux.** Structure actuelle :

```
index ──► 3 articles
ressources-demo ──► 14 articles
article-* ──► (rien, sauf retour vers ressources-demo)
```

Chaque article est un cul-de-sac. Les 11 articles non mis en avant ne reçoivent d'autorité que d'une seule page (`ressources-demo`). Or plusieurs articles se citent mutuellement dans leur texte sans être liés : `article-diagnostic-360` mentionne explicitement Ishikawa, les 5 Pourquoi, l'AMDEC et la chaîne de valeur de Porter — quatre sujets qui ont chacun leur article dédié sur le site, et aucun lien. C'est de l'autorité laissée sur la table, sur le seul levier disponible à un site sans backlink.

### Autres pages
`qui-suis-je` reste la page la mieux optimisée du site : titre porteur (« Entrepreneur & Coach Produit PME »), meta description factuelle avec noms d'entreprises (Altran, Holi, SIREM, Kaskadia), 4 H2 thématiques, parcours détaillé, lien LinkedIn sortant. Canonical propre.

---

## Points forts

- **Balisage technique de la homepage complet et sans défaut** : canonical, og:*, twitter:card, JSON-LD `ProfessionalService` + `Person` + `PostalAddress`, google-site-verification, robots.txt avec directive Sitemap et Content-Signal.
- **Redirections 301 `.html` → URL canonique confirmées** sur les pages et les articles.
- **Aucun problème www/apex détecté.**
- **Canonical propre sur les 14 articles** — aucune fuite de duplication.
- **CTA Calendly présent sur 100 % des articles** — le tunnel de conversion est en place partout.
- **14 articles de fond** couvrant un champ sémantique cohérent et interconnectable (diagnostic 360°, Ishikawa, AMDEC, 5 pourquoi, chaîne de valeur Porter, objets frontières, sales book, speedboat).
- **Le schema `Article` déjà écrit sur 3 articles est de bonne qualité** — modèle réutilisable tel quel.

## Points d'amélioration

- 🔴 **Indexation toujours nulle et toujours non vérifiée.** Cinquième semaine. Tant que Search Console n'est pas consultée, chaque audit répétera le même constat sans pouvoir l'expliquer.
- 🔴 **Maillage interne inter-articles nul (0 lien sur 14 articles).** 🆕 Le seul levier d'autorité disponible à un site sans backlink n'est pas utilisé.
- 🔴 **Zéro backlink identifié.** Le LinkedIn de Greg capte l'autorité que le site devrait capter.
- 🔴 **Aucune page de service dédiée.** Les trois créneaux SEO vides identifiés n'ont aucune page cible.
- ⚠️ **Schema `Article` absent sur 11 des 14 articles.** 🆕 Pénalise la compréhension du corpus et la citabilité par les moteurs de réponse.
- ⚠️ **H1 sans mot-clé** et **hiérarchie Hn cassée** (aucun H2 structurant sur la homepage).
- ⚠️ **`article-speedboat` absent du sitemap** — cinquième semaine de signalement.
- ⚠️ **`diagnostic 360 produit industriel` se ferme** — la SERP est passée de 1 à 6 concurrents dédiés en une semaine.

---

## Top 3 recommandations pour la semaine suivante

### 1. 🔴 Ouvrir Google Search Console — 15 minutes, cinquième relance

La balise de vérification est en place depuis plus d'un mois. Rien d'autre n'a besoin d'être fait techniquement. La seule action manquante est humaine :

- Ouvrir [search.google.com/search-console](https://search.google.com/search-console)
- Soumettre `https://intelligenceproduit.com/sitemap.xml` (Index → Sitemaps)
- Inspecter l'URL `https://intelligenceproduit.com/` → **Demander une indexation**
- Répéter pour `/qui-suis-je`, `/offres`, `/article-diagnostic-360`
- Relever dans « Pages » le nombre de pages **Valides** vs **Non indexées**, et la raison affichée
- Vérifier au passage si une propriété `www.intelligenceproduit.com` apparaît séparément

**Ce qu'on cherche à savoir :** si Google a crawlé le site et l'a écarté (et pourquoi), ou s'il ne l'a jamais découvert. Ce sont deux problèmes opposés qui appellent deux réponses opposées. Sans cette information, tout le reste est de la spéculation.

Si un rapport apparaît, en copier le résumé dans le dossier — l'audit de la semaine prochaine pourra enfin comparer autre chose que des zéros.

### 2. 🆕 Câbler le maillage interne entre articles — 45 minutes

Nouvelle recommandation, et la plus rentable des trois en rapport effort/effet. Sans backlink externe, les liens internes sont le seul signal d'autorité que le site peut s'envoyer à lui-même. Aujourd'hui il n'en envoie aucun.

Le travail est mécanique : chaque article mentionne déjà en texte des concepts qui ont leur propre page. Il suffit de transformer ces mentions en liens.

| Article source | Mentions à lier |
|---|---|
| `article-diagnostic-360` | Ishikawa → `/article-ishikawa` · 5 Pourquoi → `/article-5-pourquoi` · AMDEC → `/article-fmea-amdec` · chaîne de valeur de Porter → `/article-chaine-valeur-porter` |
| `article-ishikawa` | 5 Pourquoi, diagnostic 360°, diagnostic combiné |
| `article-5-pourquoi` | Ishikawa, AMDEC, diagnostic 360° |
| `article-fmea-amdec` | Ishikawa, diagnostic 360° |
| `article-chaine-valeur-porter` | diagnostic 360°, design PME |
| `article-diagnostic-combine` | les quatre articles méthode |

Règle simple : **3 à 5 liens sortants par article, en lien contextuel dans le corps du texte** (pas un bloc « articles liés » en pied de page, moins bien valorisé). Utiliser les URLs canoniques sans `.html` pour éviter le saut de 301.

Effet attendu : le cluster « diagnostic produit » devient lisible comme un ensemble par Google, `article-diagnostic-360` — la page cible prioritaire — passe de 2 à ~7 liens entrants, et les 11 articles orphelins remontent dans la hiérarchie de crawl.

Dans la même passe, **ajouter `article-speedboat` au sitemap** (une ligne, 5ᵉ report).

### 3. Généraliser le schema `Article` aux 11 articles restants — 30 minutes

Le modèle existe déjà dans `article-diagnostic-360.html`. Copier le bloc `<script type="application/ld+json">` dans les 11 fichiers qui n'en ont pas, en modifiant uniquement `headline`, `description` et `url`.

Pourquoi maintenant : les moteurs de réponse (ChatGPT, Perplexity, AI Overviews) s'appuient fortement sur les données structurées pour identifier auteur, date et sujet d'un contenu. C'est un canal où l'autorité de domaine pèse beaucoup moins qu'en SEO classique — donc le seul où un site neuf sans backlink peut apparaître à court terme. Le corpus de 14 articles méthodologiques est exactement le type de contenu que ces moteurs citent, à condition qu'il soit lisible par machine.

Ajouter aussi `datePublished` et `dateModified` sur les 14 (absents même des 3 balisés) — c'est un critère de fraîcheur que les moteurs de réponse utilisent pour arbitrer entre sources.

**Note sur la reco n°2 du 31 août (page `/pourquoi-mon-produit-ne-se-vend-pas`) :** elle reste valide et prioritaire à moyen terme, mais elle est reportée derrière le maillage et le schema. Raison : ces deux chantiers-là valorisent le contenu **déjà écrit** en moins de deux heures cumulées, alors que la page de service demande une demi-journée de rédaction. À faire une fois que Search Console aura dit si le site est crawlé — inutile d'écrire une page cible si le domaine n'est pas découvert.

---

## Suivi des recommandations précédentes

| Recommandation | Statut |
|---|---|
| (31 août) 1. Ouvrir Search Console | ❌ Non fait — **5ᵉ report** |
| (31 août) 2. Créer `/pourquoi-mon-produit-ne-se-vend-pas` | ❌ Non fait — **reportée volontairement** derrière les recos 2 et 3 ci-dessus |
| (31 août) 3. Réparer la hiérarchie Hn + H1 | ❌ Non fait — reste valide, déclassée en 4ᵉ position |
| (24 août) Aligner le maillage interne sur les canonicals | ❌ Non fait — mineur (301 en place) |
| (3 août) Ajouter `article-speedboat` au sitemap | ❌ Non fait — 5ᵉ report, intégré à la reco n°2 |

**Constat de méthode :** six audits, une seule recommandation appliquée. Le stock de recommandations non traitées atteint cinq entrées. J'ai donc changé de logique cette semaine : plutôt que d'empiler une nouvelle recommandation de création de contenu, les recos 2 et 3 sont des tâches **mécaniques, chiffrées, sans rédaction** (45 min + 30 min) qui valorisent l'existant. Si le temps disponible reste limité, l'ordre de priorité est : reco 1 (15 min, débloque tout le reste) → reco 2 (45 min, effet SEO direct) → reco 3 (30 min, effet moteurs de réponse).

---

## Sources consultées

- [GAYA Conseil — Diagnostic 360° pour PME industrielles](https://gayaconseil.com/diagnostic-360/)
- [ADRIA — Diagnostic à 360°, l'approche globale adaptée aux IAA](https://www.adria.tm.fr/diagnostiquer/diagnostic-a-360-lapproche-globale-adaptee-aux-iaa/)
- [XXL Stratégie — Diagnostic stratégique 360](https://xxl-strategie.fr/index.php/diagnostic-strategique-360/diagnostic-strategique-360/)
- [Coesor — Diagnostic d'Entreprise 360°](https://coesor.fr/services/diag-emergence-360/)
- [Impulsion Conseil — Diagnostic 360](https://www.impulsion-conseil.fr/diagnostic-360/)
- [KSTN — Cabinet de conseil stratégie PME Lyon](https://www.kstn.fr/cabinet-conseil-strategie-lyon.html)
- [Egnoka — Conseil stratégique PME Lyon](https://www.egnoka.fr/nos-bureaux/conseil-strategique-pme-lyon/)
- [ODICEO — Financement de l'innovation Start-up & PME Lyon](https://www.odiceo.fr/levee-de-fond-financement/)
- [Les DIGIVORES — Product Management externalisé pour PME](https://www.lesdigivores.ch/product-management-externalise-une-solution-agile-pour-les-pme-de-larc-lemanique/)
- [Yield Advisory — Agence Product Management](https://www.yieldadvisory.fr/blog/agence-product-management-pourquoi-externaliser-son-equipe-produit)
- [Opilus — Poste et mission de coach produit](https://www.opilus.fr/poste-mission-coach-produit/)
- [Morisseau Consulting — Diagnostic stratégique PME](https://www.morisseauconsulting.com/diagnostic-strategique-organisation-pme/)
- [Forum LiveMentor — Mon produit ne se vend pas](https://forum.livementor.com/t/mon-produit-ne-se-vend-pas-que-faire/898)
- [Profil LinkedIn Greg Gerard — Intelligence Produit](https://www.linkedin.com/in/gregoiregerard/)

---

*Prochain audit prévu : semaine du 14 septembre 2026*
