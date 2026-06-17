# Liquid.AI Hackathon

Landing page del hackathon **Liquid.AI** — una competencia de 48hs sobre inteligencia artificial con más de $15,000 USD en premios.

Construido con **Astro** (static site generation) y gestionado con **Bun** (sin npm/npx).

---

## Estructura

```
/
├── .github/workflows/deploy.yml   # CI/CD a GitHub Pages
├── public/
│   └── .nojekyll                  # Desactiva Jekyll en GitHub Pages
├── src/
│   ├── layouts/
│   │   └── Layout.astro           # CSS global, variables, meta tags
│   └── pages/
│       └── index.astro            # Landing page completa
├── astro.config.mjs
├── package.json
└── bun.lock
```

---

## Comandos

| Comando | Acción |
|---|---|
| `bun install` | Instalar dependencias |
| `bun run dev` | Servidor local en `http://localhost:4321` |
| `bun run build` | Build estático en `./dist/` |
| `bun run preview` | Previsualizar build local |

---

## Personalizar colores

Los colores se definen como variables CSS en `src/layouts/Layout.astro`:

| Variable | Defecto | Descripción |
|---|---|---|
| `--primary-cyan` | `#7dd3fc` | Cyan principal (links, badges, glows) |
| `--primary-blue` | `#60a5fa` | Azul secundario (gradientes, botones) |
| `--primary-glow` | `rgba(125, 211, 252, 0.4)` | Brillo de los elementos |
| `--bg-dark` | `#070b13` | Fondo principal |
| `--text-primary` | `#f8fafc` | Texto principal |

---

## Despliegue

El pipeline en `.github/workflows/deploy.yml` despliega automáticamente a GitHub Pages con cada push a `main`.

La página se sirve en: `https://laalquimia.github.io/Hackaton/`

> **Nota:** El `base` en `astro.config.mjs` debe coincidir con el nombre del repositorio (respeta mayúsculas).
