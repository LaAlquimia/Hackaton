# Guía de Desarrollo para IAs (AI Developer Guide)

Este repositorio contiene la landing page del equipo **La Alquimia** para el **Liquid.AI Hackathon**. Presenta un agente automatizado con arquitectura multi-agente bajo la temática estética **Liquid Glass (Vidrio Líquido)** en tonalidades de cyan claro.

## Stack Tecnológico
- **Framework Principal:** [Astro](https://astro.build/) (v6+) - Generación de sitio estático.
- **Gestor de Paquetes y Runtime:** [Bun](https://bun.sh/) (v1.3.14+) - Para instalación de dependencias, scripts de desarrollo y build rápido.
- **Estilos:** CSS nativo (Variables globales en CSS y scoped styles integrados en componentes Astro).

---

## Estructura del Proyecto

```bash
├── .github/workflows/deploy.yml  # Pipeline para despliegue automatizado en GitHub Pages
├── public/                       # Activos estáticos públicos (Favicon, etc.)
├── src/
│   ├── layouts/
│   │   └── Layout.astro         # Contenedor base de la aplicación (CSS global y SEO)
│   └── pages/
│       └── index.astro          # Landing page principal (diseño y scripts de interacción)
├── astro.config.mjs              # Configuración de Astro (base path y site)
├── package.json                  # Scripts y dependencias
└── bun.lockb                     # Lockfile generado por Bun
```

---

## Instrucciones para el Desarrollo

### 1. Comandos del Ciclo de Vida
* Instalar dependencias: `bun install`
* Iniciar el servidor local de desarrollo: `bun run dev`
* Compilar el sitio estático para producción: `bun run build`
* Vista previa del build localmente: `bun run preview`

### 2. Lineamientos del Diseño (Liquid Glass Theme)
La temática se basa en un diseño premium y moderno con el efecto *glassmorphism* potenciado con gradientes fluidos y formas orgánicas ("blobs") en movimiento:

- **Efecto de Vidrio:** Utilizar la clase `.glass-card`.
  ```css
  background: rgba(13, 20, 38, 0.45);
  backdrop-filter: blur(16px) saturate(140%);
  border: 1px solid rgba(255, 255, 255, 0.08);
  box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.37);
  ```
- **Esquema de Color (Light Cyan Blue):**
  - Fondo base: `#070b13`
  - Gradiente de Acento: `#67e8f9` (Cyan 300) a `#22d3ee` (Cyan 400)
  - Textos secundarios: `#94a3b8`

### 3. Configuración para Despliegues en GitHub Pages
El sitio está configurado para desplegarse automáticamente a la URL `https://LaAlquimia.github.io/Hackaton` mediante el pipeline de GitHub Actions en `.github/workflows/deploy.yml`.

---

## Secciones editables en `src/pages/index.astro`

| Sección | ID | Contenido actual |
|---|---|---|
| Hero | `#proyecto` | Presentación del equipo y el proyecto |
| Capacidades | `#capacidades` | 3 cards placeholder (editar con funcionalidades reales) |
| Tecnología | `#tecnologia` | 3 cards de arquitectura (editar con tech stack real) |
| Roadmap | `#roadmap` | Timeline de desarrollo (editar hitos reales) |
| FAQ | `#faq` | Preguntas sobre el equipo y proyecto |

- **Astro Config:** El archivo [astro.config.mjs](file:///Users/laalquimia/Projects/Hackaton/astro.config.mjs) especifica:
  - `site: 'https://LaAlquimia.github.io'`
  - `base: '/hackaton'`
  - `output: 'static'`
- Si cambias el dominio de destino, actualiza el valor `site` en `astro.config.mjs`.
