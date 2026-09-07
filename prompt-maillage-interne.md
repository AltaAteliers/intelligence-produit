# Prompt — Maillage interne des articles (intelligenceproduit.com)

> Copier tout ce qui suit la ligne de séparation dans une session Claude ayant accès au dossier `SITE WEB`.
> Le prompt est autonome : il décrit le corpus, les règles, l'architecture cible et applique les modifications directement.

---

Tu travailles sur le site statique **intelligenceproduit.com** (HTML pur, déployé sur Cloudflare Pages, repo `AltaAteliers/intelligence-produit`). Les fichiers sont dans le dossier de travail connecté.

## Mission

Câbler le maillage interne entre les 14 articles du site. Aujourd'hui **aucun article ne pointe vers un autre article** : chaque page est un cul-de-sac. Le site n'ayant aucun backlink externe, le maillage interne est le seul levier d'autorité disponible, et il n'est pas utilisé.

**Applique les modifications directement dans les fichiers.** Pas de validation intermédiaire — je relirai avec `git diff`. Termine par un compte rendu.

## Corpus (14 articles)

| Fichier | Sujet | URL canonique |
|---|---|---|
| `article-diagnostic-360.html` | Méthode de diagnostic produit à 360° — chaîne de valeur, Ishikawa, 5 Pourquoi, AMDEC, signaux SAV | `/article-diagnostic-360` |
| `article-chaine-valeur-porter.html` | Chaîne de valeur de Porter appliquée au produit | `/article-chaine-valeur-porter` |
| `article-ishikawa.html` | Diagramme d'Ishikawa, les 5M + Milieu | `/article-ishikawa` |
| `article-5-pourquoi.html` | Les 5 Pourquoi, cause racine | `/article-5-pourquoi` |
| `article-fmea-amdec.html` | AMDEC, priorisation des défaillances | `/article-fmea-amdec` |
| `article-diagnostic-combine.html` | Combiner Porter + Ishikawa + AMDEC + 5 Pourquoi | `/article-diagnostic-combine` |
| `article-design-pme.html` | Le design comme investissement rentable en PME | `/article-design-pme` |
| `article-keep-it-simple.html` | Règles d'or du design produit (Hartmut Esslinger) | `/article-keep-it-simple` |
| `article-voir-autrement.html` | Changer de regard pour réussir | `/article-voir-autrement` |
| `article-objets-frontieres.html` | Objets frontières — aligner marketing, R&D, commerce | `/article-objets-frontieres` |
| `article-speedboat.html` | Atelier SpeedBoat — faire remonter les freins | `/article-speedboat` |
| `article-product-manager-entre-2-chaises.html` | Le product manager entre deux chaises | `/article-product-manager-entre-2-chaises` |
| `article-sales-book.html` | Le sales book pour les commerciaux | `/article-sales-book` |
| `article-build-it-yourself.html` | L'IA change la logique du logiciel en PME/PMI | `/article-build-it-yourself` |

## Architecture cible : 3 clusters hub-and-spoke

Les hubs sont les 3 articles déjà mis en avant sur la homepage (ce sont eux qui reçoivent le plus d'autorité, ils doivent la redistribuer et la recevoir en retour).

**Cluster 1 — Diagnostic produit** · hub : `article-diagnostic-360`
Spokes : `chaine-valeur-porter`, `ishikawa`, `5-pourquoi`, `fmea-amdec`, `diagnostic-combine`

**Cluster 2 — Conception & design** · hub : `article-design-pme`
Spokes : `keep-it-simple`, `voir-autrement`, `build-it-yourself`

**Cluster 3 — Organisation & alignement** · hub : `article-objets-frontieres`
Spokes : `speedboat`, `product-manager-entre-2-chaises`, `sales-book`

Règles de circulation :

- Chaque **spoke** pointe vers son hub (lien obligatoire) + 1 à 3 spokes voisins du même cluster.
- Chaque **hub** pointe vers l'ensemble de ses spokes.
- **2 à 3 liens inter-clusters** au total, pas plus, pour éviter de diluer la thématique. Exemples pertinents : `diagnostic-360` → `sales-book` (le commerce est un maillon de la chaîne diagnostiquée) ; `objets-frontieres` → `diagnostic-360` (l'alignement interne est souvent une cause racine) ; `voir-autrement` → `diagnostic-360`.
- **Cible prioritaire : `article-diagnostic-360`.** C'est la page qui vise le mot-clé le plus accessible du portefeuille (« pourquoi mon produit ne se vend pas »). Elle doit finir avec le plus grand nombre de liens entrants du corpus — vise 6 minimum.

## Règles d'écriture des liens

1. **3 à 5 liens sortants par article**, jamais plus. Au-delà, chaque lien perd de sa valeur et le texte devient illisible.
2. **Liens contextuels dans le corps du texte uniquement.** Pas de bloc « articles liés » en pied de page : moins bien valorisé par Google et par les moteurs de réponse.
3. **Ancre descriptive, jamais générique.** Interdits : « ici », « cet article », « en savoir plus », « lire ». L'ancre doit contenir le sujet de la page cible — par exemple `le diagramme d'Ishikawa`, `remonter à la cause racine avec les 5 Pourquoi`, `une AMDEC`.
4. **Varie les ancres** vers une même cible d'un article à l'autre. Ne répète pas la même formulation exacte partout.
5. **Un seul lien par cible et par article.** Si un concept est mentionné plusieurs fois, lie la première occurrence naturelle.
6. **URLs canoniques sans `.html`** — écris `href="/article-ishikawa"`, pas `href="article-ishikawa.html"`. Cloudflare Pages redirige les `.html` en 301 : les éviter économise un saut de crawl sur chaque lien.
7. **Ne réécris pas la prose.** Les mentions à lier existent déjà en texte brut. Ton travail est d'entourer un fragment existant d'une balise `<a>`, pas de reformuler. Si aucune mention naturelle n'existe pour un lien de l'architecture cible, tu peux ajouter **une** phrase courte de transition en fin de section — mais privilégie toujours l'existant.
8. **Ne touche pas** à la navigation, au `<div class="callout">`, au `.back-link`, au CTA Calendly, aux balises `<head>`, ni au JSON-LD.

### Point de vigilance CSS — obligatoire

Les articles contiennent la règle globale `a{ color:inherit; text-decoration:none; }`. Sans correctif, **tout lien ajouté dans le corps du texte serait invisible** (même couleur que le texte, sans soulignement).

Ajoute donc dans le `<style>` de **chaque article modifié**, à la suite de la règle `.content p`, la déclaration :

```css
.content p a, .content li a{ color:var(--indigo); text-decoration:underline; text-underline-offset:2px; text-decoration-thickness:1px; }
.content p a:hover, .content li a:hover{ opacity:.75; }
```

Vérifie que la variable `--indigo` est bien définie dans le fichier ; sinon utilise la valeur littérale employée par `.cat`.

## Tâche annexe

Ajoute `article-speedboat` au `sitemap.xml`. Il en est absent depuis le 3 août alors que l'article est en ligne. Une entrée `<url>` avec `changefreq: monthly` et `priority: 0.7`, au format des autres articles.

## Ordre d'exécution

1. Lis les 14 articles et relève, pour chacun, les mentions en texte brut qui correspondent à une autre page du corpus.
2. Établis le plan de liens complet (source → cible → ancre exacte) et vérifie qu'il respecte l'architecture et les quotas.
3. Applique les modifications : liens + bloc CSS dans chaque fichier touché.
4. Mets à jour `sitemap.xml`.
5. Vérifie.

## Vérification finale — ne conclus pas sans l'avoir faite

- Compte les liens sortants et entrants par article ; vérifie que chaque article a entre 3 et 5 sortants et **au moins 1** entrant.
- Vérifie qu'aucun `href` ne contient `.html` parmi les liens ajoutés.
- Vérifie qu'aucun article ne se lie à lui-même.
- Vérifie que le bloc CSS est présent dans chaque fichier modifié.
- Vérifie que le sitemap contient bien 20 URLs et reste un XML valide.
- Lance `git diff --stat` et relis le diff d'au moins deux fichiers pour confirmer qu'aucune prose n'a été altérée.

## Compte rendu attendu

- Tableau récapitulatif : article → nombre de liens sortants → nombre de liens entrants.
- La liste des liens inter-clusters retenus, avec une ligne de justification chacun.
- Les cas où tu as dû ajouter une phrase plutôt que d'utiliser une mention existante, avec la phrase ajoutée.
- Tout écart assumé par rapport aux règles ci-dessus, et pourquoi.
