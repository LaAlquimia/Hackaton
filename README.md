# La Alquimia — Agente Autónomo Liquid Glass

Página del equipo **La Alquimia**, participantes del **Liquid.AI Hackathon 2026**. Presentamos nuestro agente automatizado con arquitectura multi-agente e interfaz liquid glass.

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

Los colores se definen como variables CSS en `src/layouts/Layout.astro` (paleta **light cyan blue**):

| Variable | Defecto | Descripción |
|---|---|---|
| `--primary-cyan` | `#67e8f9` | Cyan claro principal (links, badges, glows) |
| `--primary-blue` | `#22d3ee` | Cyan medio (gradientes, botones) |
| `--primary-glow` | `rgba(103, 232, 249, 0.4)` | Brillo de los elementos |
| `--bg-dark` | `#070b13` | Fondo principal |
| `--text-primary` | `#f8fafc` | Texto principal |

---

## Despliegue

El pipeline en `.github/workflows/deploy.yml` despliega automáticamente a GitHub Pages con cada push a `main`.

La página se sirve en: `https://laalquimia.github.io/Hackaton/`

> **Nota:** El `base` en `astro.config.mjs` debe coincidir con el nombre del repositorio (respeta mayúsculas).

---

## Contenido a personalizar (TBD)

El equipo aún debe definir:

- **Nombre del agente automatizado** — actualmente referido como "agente autónomo"/"agente automatizado"
- **Funcionalidades concretas** — los placeholders en Capacidades, Tecnología y Roadmap son editables en `src/pages/index.astro`
- **Enlaces de redes sociales** — los enlaces a GitHub apuntan a `https://github.com/LaAlquimia`
