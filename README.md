<div align="center">

# 🌊 Microplastic Pollution Crisis

**An interactive environmental awareness web page about microplastic pollution — built with Vue 3 and Vite.**

[![Vue](https://img.shields.io/badge/Vue-3-42b883?logo=vue.js&logoColor=white)](https://vuejs.org)
[![Vite](https://img.shields.io/badge/Vite-8-646cff?logo=vite&logoColor=white)](https://vite.dev)
[![License](https://img.shields.io/badge/license-MIT-lightgrey)](#license)

</div>

---

## Overview

A visually rich, fully animated single-page site that educates visitors on the microplastic pollution crisis — what microplastics are, why they matter, and what individuals can do about it. Built as an environmental awareness project using Vue 3's component model and Vite for fast development and bundling.

The standout visual feature is a full-screen animated ocean background: layered SVG wave paths, rising bubbles, underwater light rays, floating microplastic particles, and eight individually colored CSS-animated fish swimming across the scene — all purely CSS and SVG, no canvas or third-party animation library.

## ✨ Features

- 🌊 **Animated ocean scene** — layered SVG waves, rising bubbles, light rays, floating particles, and swimming fish, all in pure CSS
- 📊 **Key stats hero** — 5mm particle size, 5 trillion ocean particles, 100+ year decomposition time, displayed in a glassmorphism stat bar
- 🃏 **Three content cards** with staggered entrance animations:
  - **Topic** — what microplastics are and how they spread
  - **Info** — why it matters, with an impact grid (wildlife, pollution, longevity)
  - **Tips** — 5 numbered practical actions readers can take today
- 📱 **Responsive** — mobile layout adjustments at 768px breakpoint
- 🎨 **Design system** — ocean-themed CSS custom properties (`--ocean-deepest` through `--ocean-foam`, `--coral`, `--sand`)
- 🔤 **Google Fonts** — Outfit (headings) + Manrope (body)

## 🛠 Tech Stack

- **[Vue 3](https://vuejs.org)** with `<script setup>` SFCs
- **[Vite](https://vite.dev)** for development server and production builds
- Pure CSS animations (no animation library)
- No CSS framework — all styles are scoped per-component or defined as global design tokens in `App.vue`

## 🚀 Getting Started

```bash
npm install
npm run dev
```

Open `http://localhost:5173` in your browser. The page is fully static — no backend, no API calls.

### Other commands

```bash
npm run build    # production build → dist/
npm run preview  # preview the production build locally
```

## 📂 Project Structure

```
microplastic-awareness/
├── index.html              # Entry HTML — sets the page title
├── vite.config.js          # Vite config with Vue plugin
├── src/
│   ├── main.js             # App entry point
│   ├── App.vue             # Root component: ocean scene, hero, layout, global styles
│   └── components/
│       ├── Topic.vue       # "What are microplastics?" card
│       ├── Info.vue        # "Why it matters" card with impact grid
│       └── Tips.vue        # "Environmental Tips" card with numbered action list
└── public/
    ├── favicon.svg
    └── icons.svg
```

## 🗺 Roadmap

- [ ] Smooth scroll navigation between sections
- [ ] Intersection Observer for scroll-triggered card animations (currently entrance-only)
- [ ] Dark/light mode toggle
- [ ] Additional sections: sources, quiz, shareable pledge
- [ ] Vue Router for multi-page expansion (e.g., a dedicated "Take Action" page)

## License

[MIT](https://opensource.org/licenses/MIT)
