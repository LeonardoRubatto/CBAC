# Simulateur Bac

> Simulateur de moyenne du baccalauréat gratuit — coefficients officiels 2026–2027  
> Domaine : https://bac.wecalc.fr · Langue : fr · Catégorie : Éducation · Accent : `#0F766E`

## Fonctionnalités

- Calcul de la moyenne générale au baccalauréat général (EG, spécialités, Grand Oral, options) avec coefficients officiels 2026–2027
- Calcul de la moyenne au baccalauréat technologique (toutes séries STI2D, STMG, ST2S, STL, STAV, STD2A, STHR) avec coefficients par série
- Détection automatique de la mention (Sans mention, Assez Bien, Bien, Très Bien) et du seuil de rattrapage
- Simulation d'objectifs : calcul de la note minimale à obtenir dans une matière pour atteindre une mention cible
- Partage de résultat par URL encodée, export PDF, dark mode, cookie banner RGPD, responsive mobile
- 4 blocs JSON-LD : `WebApplication`, `WebSite`, `BreadcrumbList`, `FAQPage` — rich results Google activés

## Structure des fichiers

```
CBAC/
├── index.html
├── confidentialite.html
├── 404.html
├── _headers
├── robots.txt
├── sitemap.xml
├── readme.md
├── favicon.png
├── apple-touch-icon.png
├── og-image.png
└── assets/
    └── icons/
        ├── logo-fibo4.svg
        ├── bonus.svg
        ├── europe.svg
        ├── exam.svg
        ├── france.svg
        ├── info.svg
        ├── pdf.svg
        ├── share.svg
        ├── sources.svg
        ├── sources-dark.svg
        ├── success.svg
        ├── theme-dark.svg
        ├── theme-light.svg
        └── warning.svg
```

## Icônes SVG requises

Installer dans `/assets/icons/` : `logo-fibo4.svg`, `bonus.svg`, `europe.svg`, `exam.svg`, `france.svg`, `info.svg`, `pdf.svg`, `share.svg`, `sources.svg`, `sources-dark.svg`, `success.svg`, `theme-dark.svg`, `theme-light.svg`, `warning.svg`

## Sources des données

| Source | Organisme | URL | Vérifié le |
|--------|-----------|-----|------------|
| Coefficients baccalauréat général 2026–2027 | Ministère de l'Éducation nationale | https://www.education.gouv.fr/le-baccalaureat-general-36467 | 2026-03-19 |
| Coefficients baccalauréats technologiques 2026–2027 | Ministère de l'Éducation nationale | https://www.education.gouv.fr/le-baccalaureat-technologique-36468 | 2026-03-19 |
| Règles de mention et de rattrapage | Ministère de l'Éducation nationale | https://www.education.gouv.fr | 2026-03-19 |
| Épreuves du Grand Oral — coefficient et modalités | Ministère de l'Éducation nationale | https://www.education.gouv.fr/le-grand-oral-326198 | 2026-03-19 |

## Déploiement

Push GitHub → Cloudflare Pages. Aucun outil de build. Le dossier `CBAC/` est la racine du site.

```bash
git add .
git commit -m "update: [description courte]"
git push origin main
```

Cloudflare Pages détecte le push et redéploie automatiquement en ~30 secondes.

## Mise à jour des données

- Fréquence recommandée : annuelle — vérifier en septembre (arrêtés ministériels de rentrée scolaire)
- Prochaine vérification : septembre 2026
- Fichiers à mettre à jour : `index.html` (coefficients dans `CFG`, année scolaire dans le title), `sitemap.xml` (`lastmod`)

## Assets graphiques à produire manuellement

| Fichier | Dimensions | Contenu |
|---------|------------|---------|
| `favicon.png` | 32×32 px | Fond `#0F766E`, lettres **NB** en blanc, bold, centré |
| `apple-touch-icon.png` | 180×180 px | Même design — iOS arrondit automatiquement les coins |
| `og-image.png` | 1200×630 px | Fond `#dde6ef`, card blanche centrée : logo + "Simulateur Bac 2026–2027 — Calcul de moyenne officiel, mention et rattrapage" |

