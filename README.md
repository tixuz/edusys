# EduSys — IT Management Platform for Education Systems

A single-page marketing site for **EduSys**, a platform targeting IT managers of national education management systems such as [OpenEMIS](https://www.openemis.org/).

## Live Demo

Deployed via GitHub Pages → **https://tixuz.github.io/edusys**

## What's Inside

| Section | Description |
|---------|-------------|
| **Hero** | Headline + live EMIS dashboard mockup card |
| **Services** | Asymmetric grid — featured sysadmin card + 5 satellite services |
| **How It Works** | 4-step numbered process timeline |
| **Testimonials** | 3 quotes from education IT directors |
| **Case Studies** | 3 real-world EMIS deployment stories |
| **CTA + Form** | Discovery call request form |
| **Chat Widget** | Floating AI assistant styled to OpenEMIS KB Docs theme |

## Design System

- **Dark / Light theme toggle** — remembers preference via `localStorage`, respects `prefers-color-scheme`
- **Colors** — OKLCH palette based on the cleancoders-design system; warm dark `oklch(19% 0.015 60)`, teal accent `#1276a2 / #53bceb`
- **Typography** — `calps-black` (cleancoders.com CDN) for headings, `Roboto` for body
- **Animations** — AOS (Animate On Scroll) for scroll reveals; custom CSS keyframes for hero drift, pulse ring, nudge
- **Chat widget** — Ice-glass backdrop-filter panel, matching OpenEMIS KB Docs visual language

## Stack

- Pure HTML + CSS (no framework, no build step)
- [AOS](https://michalsnik.github.io/aos/) for scroll animations
- [Font Awesome 6](https://fontawesome.com/) for icons
- Deployed on **GitHub Pages**

## Local Development

```bash
# Serve with any static server — e.g.:
python3 -m http.server 3000
# → open http://localhost:3000
```

Or with Node:

```bash
npx serve .
```

## Deploy

Deployed automatically via GitHub Pages from the `main` branch root.

To manually redeploy after changes:

```bash
git add index.html
git commit -m "update site"
git push origin main
```

## License

MIT — see [LICENSE](./LICENSE)
