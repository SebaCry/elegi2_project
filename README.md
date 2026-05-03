# ELEGI2 — Landing

> Porque no lo elegimos nosotros a Él.

Landing oficial del proyecto **Elegi2** — tres voces, un propósito. Construida con Astro 6, Tailwind CSS 4 y `tailwindcss-animated`. Diseño editorial minimalista en negro + crema, con tipografía Anton + Cormorant Garamond + Inter.

## Stack

- **Framework:** [Astro 6](https://astro.build) (static)
- **Estilos:** [Tailwind CSS 4](https://tailwindcss.com) vía `@tailwindcss/vite`
- **Animaciones:** [`tailwindcss-animated`](https://github.com/new-data-services/tailwindcss-animated) + reveal en scroll con IntersectionObserver
- **Tipografías:** Anton (display), Cormorant Garamond (serif), Inter (sans) — desde Google Fonts

## Desarrollo

```bash
npm install
npm run dev          # http://localhost:4321
npm run build        # build estático en dist/
npm run preview      # preview del build
```

Requiere Node ≥ 22.12.

## Estructura

```
src/
├── layouts/Layout.astro          → fuentes, SEO, IntersectionObserver
├── components/
│   ├── Nav.astro · Footer.astro
│   ├── Hero.astro                → Capítulo inicial
│   ├── QuienesSomos.astro        → 01 — Quiénes somos
│   ├── Proposito.astro           → 02 — Propósito (3 pilares)
│   ├── Recursos.astro            → 03 — Recursos bíblicos
│   ├── Blog.astro                → 04 — Blog editorial
│   ├── Eventos.astro             → 05 — Eventos
│   ├── Oracion.astro             → 06 — Pedidos de oración
│   ├── Testimonios.astro         → 07 — Testimonios
│   └── Contacto.astro            → 08 — Contáctanos para orar
├── pages/index.astro             → orquesta secciones
└── styles/global.css             → tokens de diseño + utilities
```

Imágenes del branding en `public/img/`.

## Deploy en Cloudflare Pages

Conectar este repo en el dashboard de Cloudflare Pages con:

| Campo | Valor |
|---|---|
| Framework preset | Astro |
| Build command | `npm run build` |
| Build output directory | `dist` |
| Root directory | *(vacío — la raíz del repo)* |
| Node version | `22` (env var `NODE_VERSION=22`) |

## Pendientes (frontend completo, falta integrar backend)

- [ ] Conectar formulario de pedidos de oración a backend (Resend / Formspree / Supabase)
- [ ] Conectar formulario de contacto
- [ ] Conectar suscripción al newsletter
- [ ] Reemplazar foto placeholder del 3er influencer (Camilo)
- [ ] Mover datos hardcodeados (versículos, eventos, artículos) a `src/content/`

---

© Elegi2 · Colombia
