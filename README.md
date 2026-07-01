<div align="center">

# 🌊 OceanWatch

### Microplastic Pollution Awareness

**A fully animated environmental awareness site built with Vue 3 and Vite — no animation library, just pure CSS and SVG.**

[![Vue](https://img.shields.io/badge/Vue-3-42b883?logo=vue.js&logoColor=white)](https://vuejs.org)
[![Vite](https://img.shields.io/badge/Vite-8-646cff?logo=vite&logoColor=white)](https://vite.dev)
[![License](https://img.shields.io/badge/license-MIT-lightgrey)](#license)

<br/>

> _Add a screenshot or screen recording here once you have the app running_
>
> ```md
> <img src="docs/preview.png" width="800" alt="OceanWatch preview" />
> ```

</div>

---

## What is this?

OceanWatch is a single-page environmental awareness site about the microplastic pollution crisis — what microplastics are, why they're dangerous, and what everyday people can do about it.

The headline feature is a full-screen animated ocean built entirely in pure CSS and SVG: layered wave paths, rising bubbles, underwater light rays, floating microplastic particles, and eight individually colored fish swimming across the scene. No canvas, no GSAP, no animation library — just keyframes.

## ✨ Features

- 🌊 **Animated ocean background** — SVG waves, rising bubbles, underwater light rays, floating particles, and 8 CSS-animated fish, all without a single animation library
- 📊 **Hero stat bar** — key facts (5mm size limit, 5 trillion ocean particles, 100+ year decomposition) in a glassmorphism card
- 🃏 **Three staggered content cards:**
  - `Topic.vue` — what microplastics are and how they spread globally
  - `Info.vue` — why it matters, with an impact grid covering wildlife, pollution, and longevity
  - `Tips.vue` — 5 numbered, practical actions readers can take today
- 🎨 **Ocean design system** — a full set of CSS custom properties (`--ocean-deepest` → `--ocean-foam`, `--coral`, `--sand`) for consistent theming across all components
- 🔤 **Outfit + Manrope** via Google Fonts — display heading weight paired with a clean readable body font
- 📱 **Responsive** — mobile breakpoints at 768px, stacked layouts, scaled typography

## 🛠 Tech Stack

| Tool | Role |
|---|---|
| [Vue 3](https://vuejs.org) | Component model, SFCs with `<script setup>` |
| [Vite 8](https://vite.dev) | Dev server, HMR, production bundling |
| Pure CSS | All animations — `@keyframes`, `animation-delay`, CSS custom properties |
| Scoped `<style>` | Per-component styles via Vue's scoped style blocks |

No UI framework. No CSS library. No animation dependency.

## 🚀 Getting Started

```bash
git clone https://github.com/bmf-19/OceanWatch.git
cd OceanWatch
npm install
npm run dev
```

Open [`http://localhost:5173`](http://localhost:5173) in your browser.

### All commands

```bash
npm run dev      # start dev server with hot reload
npm run build    # production build → dist/
npm run preview  # preview the production build locally
```

## 📂 Project Structure

```
OceanWatch/
├── index.html               # Page entry — title, meta, root div
├── vite.config.js           # Vite + Vue plugin config
├── src/
│   ├── main.js              # Mounts the Vue app
│   ├── App.vue              # Root: ocean scene, hero section, layout, global design tokens
│   └── components/
│       ├── Topic.vue        # "What are microplastics?" — definition + key fact callout
│       ├── Info.vue         # "Why it matters" — 3-item impact grid + action paragraph
│       └── Tips.vue         # "Environmental Tips" — numbered action list (5 tips)
└── public/
    ├── favicon.svg
    └── icons.svg
```

## 🎨 Design Highlights

The animated ocean scene is built entirely from HTML elements and CSS — no `<canvas>`, no WebGL, no JavaScript animation loop:

- **Waves** — three layered SVG `<path>` elements with staggered `wave-motion` keyframes at different durations (10s, 12s, 14s) create natural interference patterns
- **Bubbles** — 20 `div` elements with `rise` keyframes, each sized and timed independently via `nth-child` selectors
- **Light rays** — 5 absolutely positioned divs with `sway-light` keyframes, giving the underwater shimmer effect
- **Fish** — 8 CSS-only fish shapes using `border-radius` + `::before`/`::after` pseudo-elements for the tail and eye, animated with a `swim` keyframe that moves them across the full viewport width

## 🗺 Roadmap

- [ ] Scroll-triggered card animations via Intersection Observer (currently entrance-only)
- [ ] Smooth scroll navigation between sections
- [ ] Dark / light mode toggle
- [ ] Additional sections: cited sources, interactive quiz, shareable pledge
- [ ] Vue Router for multi-page expansion (dedicated "Take Action" page)
- [ ] Migrate animations to `prefers-reduced-motion` safe defaults

## License

[MIT](https://opensource.org/licenses/MIT)
