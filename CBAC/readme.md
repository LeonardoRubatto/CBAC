# NoteBac — Simulateur de moyenne du baccalauréat

**Domaine :** calculateur-note-bac.fr  
**Langue :** Français  
**Catégorie :** education  
**Accent :** #0F766E (teal)

## Description

Simulateur de moyenne du baccalauréat général et technologique standard, déployé sur Cloudflare Pages via GitHub.

- Session 2026 : coefficients en vigueur, Grand oral 10 (G) / 14 (T)
- Session 2027+ : mathématiques anticipées (coeff. 2), Grand oral abaissé à 8 (G) / 12 (T)
- Contrôle continu obligatoire (40 %) avec arrondi réglementaire au dixième supérieur
- Épreuves anticipées et terminales (60 %) avec coefficients officiels par voie
- Options facultatives : jusqu'à 4 options standard + latin + grec, scope 1re / terminale / les deux
- Simulation du rattrapage (second groupe) : substitution oral > écrit sur 2 matières distinctes
- Seuils & écarts : points manquants vers 8 / 10 / 12 / 14 / 16 / 18

## Structure

```
calculateur-note-bac/
├── index.html             Calculateur principal
├── confidentialite.html   Mentions légales, RGPD, conditions, contact
├── 404.html               Page d'erreur
├── _headers               En-têtes de sécurité Cloudflare
├── robots.txt
├── sitemap.xml
├── readme.md
├── favicon.png            32×32 — à produire (voir Assets graphiques)
├── apple-touch-icon.png   180×180 — à produire (voir Assets graphiques)
├── og-image.png           1200×630 — à produire (voir Assets graphiques)
└── assets/
    └── icons/
        ├── warning.svg
        ├── info.svg
        ├── error.svg
        ├── success.svg
        ├── share.svg
        ├── pdf.svg
        ├── sources.svg
        ├── sources-dark.svg
        ├── theme-dark.svg
        ├── theme-light.svg
        └── france.svg
```

## Icônes

Installer les fichiers SVG dans `/assets/icons/` avant déploiement.

## Assets graphiques

Ces fichiers ne sont pas générés automatiquement. Ils sont à créer avant déploiement.

| Fichier | Dimensions | Contenu |
|---|---|---|
| `favicon.png` | 32×32 px | Fond `#0F766E` (teal), lettres **NB** en blanc, bold, centré |
| `apple-touch-icon.png` | 180×180 px | Même design que favicon — iOS ajoute automatiquement les coins arrondis |
| `og-image.png` | 1200×630 px | Fond `#dde6ef`, card blanche centrée avec logo NB + "Simulateur Bac" + "Calculateur de moyenne officiel 2026–2027" |

Générateur recommandé : [realfavicongenerator.net](https://realfavicongenerator.net)

## Sources des données

- Ministère de l'Éducation nationale — Comment calculer votre note au baccalauréat (03/12/2025)
- Éduscol — Le contrôle continu des candidats scolaires au baccalauréat général ou technologique
- Éduscol — Les épreuves terminales du baccalauréat général
- Éduscol — Les épreuves terminales du baccalauréat technologique
- Légifrance — Code de l'éducation, art. D334-8 et D336-8
- Décret n°2025-513 du 10 juin 2025 (réforme session 2027)
- Décret n°2025-1159 du 4 décembre 2025 (points jury, session 2026)

## Déploiement

Push sur GitHub → Cloudflare Pages build automatique.  
Aucun outil de build requis — HTML/CSS/JS pur.

## Mise à jour des données

Vérifier les coefficients au minimum 1 fois par an avant chaque session.  
Surveiller tout décret, arrêté ou note de service modifiant les coefficients, seuils ou structure d'épreuve.  
Prochaine vérification recommandée : mars 2027.
