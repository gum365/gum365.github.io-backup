# GUM365 — Astro + Velocity + OKF

Site GitHub Pages de la communauté GUM365.

## Architecture

- **Astro 6** pour la génération statique.
- **Velocity** comme couche de présentation, en reprenant les mêmes principes de design et les mêmes tokens que les implémentations MuBrain et georgeault.github.io.
- **OKF** comme source unique de contenu dans `knowledge/okf`.
- **FR_CA** comme source de vérité éditoriale.
- **EN_CA** comme traduction liée par `translation_key`.
- Mode **clair / sombre** persistant.
- Déploiement automatique vers **GitHub Pages** depuis `master`.

Les pages ne sont pas dupliquées dans `src/content`. Astro charge directement les fichiers Markdown OKF depuis `knowledge/okf`.

```
knowledge/okf/
├── fr-CA/
│   ├── index.md
│   ├── communaute.md
│   ├── evenements.md
│   └── a-propos.md
└── en-CA/
    ├── index.md
    ├── community.md
    ├── events.md
    └── about.md
```

## Développement

```bash
pnpm install
pnpm dev
pnpm build
```
