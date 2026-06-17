# Liquid.AI Hackathon Landing Page

Este proyecto está construido con **Astro** y gestionado completamente con **Bun** (sin dependencias ni scripts de npm o npx).

## 🚀 Estructura del Proyecto

Dentro del proyecto verás las siguientes carpetas y archivos principales:

```text
/
├── .github/workflows/deploy.yml # Pipeline de despliegue automático a GitHub Pages
├── public/                      # Activos estáticos públicos
├── src/
│   ├── layouts/
│   │   └── Layout.astro         # Contenedor base de la aplicación (CSS global y SEO)
│   └── pages/
│       └── index.astro          # Landing page principal (diseño y scripts de interacción)
├── astro.config.mjs             # Configuración de Astro (base path y site)
├── package.json                 # Definición de dependencias y scripts de ejecución
└── bun.lock                     # Archivo de bloqueo exclusivo de Bun
```

---

## 🧞 Comandos con Bun

Todos los comandos deben ejecutarse desde la raíz del proyecto utilizando `bun`:

| Comando | Acción |
| :--- | :--- |
| `bun install` | Instala todas las dependencias del proyecto |
| `bun run dev` | Inicia el servidor de desarrollo local en `http://localhost:4321` |
| `bun run build` | Compila el sitio estático para producción en `./dist/` |
| `bun run preview` | Previsualiza el build estático localmente |
| `bun x astro ...` | Ejecuta comandos CLI de Astro directamente |

---

## 🛠️ Configuración de Despliegue

El despliegue está automatizado con GitHub Actions en cada push a las ramas principales (`main` o `master`).

Para cambiar la URL de tu sitio, edita la propiedad `site` en [astro.config.mjs](file:///Users/laalquimia/Projects/Hackaton/astro.config.mjs).
