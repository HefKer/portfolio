# hefker.dev

My personal portfolio. Astro + Tailwind v4 + daisyUI static site, deployed on Cloudflare Pages.

Live: <https://hefker.dev>

## Stack

- **Astro 6** (TypeScript, strict mode)
- **Tailwind CSS 4** via `@tailwindcss/vite` (CSS-first config — no `tailwind.config.js`)
- **daisyUI 5** with a custom `hefker` theme + auto dark variant (`prefersdark`)
- **Fontsource** for self-hosted Inter + Fraunces (no Google CDN)
- Static HTML

## Project structure

```
src/
  layouts/
    Base.astro          # html shell, head meta, background, footer
  components/
    Background.astro    # fixed dot-grid + soft gradient
    Hero.astro
    ProjectCard.astro
    Projects.astro
    About.astro
    Contact.astro
  pages/
    index.astro         # landing
    resume.astro        # placeholder
  styles/
    global.css          # Tailwind entry + daisyUI themes + typography
public/                 # static assets served at root
```

## Commands

Package manager: **pnpm** (required — `pnpm-workspace.yaml` configures the esbuild/sharp build allowlist). Node `>=22.12.0`.

| Command | Action |
|---|---|
| `pnpm install` | Install deps |
| `pnpm dev` | Dev server at `localhost:4321` |
| `pnpm build` | Production build to `./dist/` |
| `pnpm preview` | Serve built `./dist/` locally |
| `pnpm astro check` | Type-check `.astro` files |
| `pnpm astro add <integration>` | Add Astro integration |

## Deploy

Cloudflare Pages auto-builds on push to `main`. PR branches get preview deploys. No CI config yet.

## Roadmap

1. ✅ Foundation: scaffold, deploy, custom domain
2. ✅ v1 content: Hero, Projects, About, Contact, footer
3. Resume page + sitemap + OG image
4. `/notes` via Astro Content Collections
5. Polish: `/uses`, Lighthouse >95, one justified framework island
