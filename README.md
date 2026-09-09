# Cafe TeeKaapi — v2 (Where Great Days Begin)

Warm, elegant brunch-café site: handcrafted coffee, delicious brunch, and warm
hospitality — all day, every day. Est. 2017.

## Stack

- [Astro 5](https://astro.build) with view transitions (`ClientRouter`)
- [Tailwind CSS 4](https://tailwindcss.com) via `@tailwindcss/vite` — classes co-located in templates
- `@astrojs/sitemap`

## Commands

```bash
npm install
npm run dev      # http://localhost:4321
npm run build
npm run preview
```

## Theming

Brand colours are defined once in `src/styles/global.css` under `@theme`.
Swap `--color-primary` / `--color-secondary` (plus `-strong` / `-soft` steps)
to rebrand the whole site — every utility (`bg-primary`, `text-secondary`, …)
resolves from these tokens.

Dark mode: `data-theme="dark"` on `<html>`, toggled in the header, persisted
to `localStorage`, defaults to `prefers-color-scheme`. An inline head script
prevents any flash of the wrong theme.

## Quality checklist

- Light & dark modes · view transitions · scroll-reveal animations
  (all motion disabled under `prefers-reduced-motion`)
- Skip link, landmarks, labelled controls, focus-visible styles
- Canonical, Open Graph, Twitter cards, JSON-LD, sitemap, robots.txt
- Responsive from 320px; lazy images with width/height set

## Pages

`/` home · `/about` · `/menu` · `/locations` · `/contact` · custom 404
