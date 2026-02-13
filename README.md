# OMM

Este es el repositorio de la nueva página web de la Olimpiada Michoacana de Matemáticas. 

## TL;DR

```sh
# One-liner (asume que Bun ya está instalado):
git clone https://github.com/OlimpiadaMatematicasMichoacan/webpage.git && cd webpage && bun install && bun run dev

# One-liner TODO-ALL (instala Bun, clona, instala deps y arranca) — macOS / Linux:
curl -fsSL https://bun.com/install | bash && export BUN_INSTALL="$HOME/.bun"; export PATH="$BUN_INSTALL/bin:$PATH"; git clone https://github.com/OlimpiadaMatematicasMichoacan/webpage.git && cd webpage && bun install && bun run dev
```


## Features
- [Lighthouse Score: 100](https://pagespeed.web.dev/analysis/https-roicort-github-io-launchpad/xthz1r5i4v?form_factor=mobile)
- Blog with Markdown/MDX, featured post, and tag listings
- Typed collections for posts, authors, and socials in [src/content.config.ts](src/content.config.ts)
- Site-wide search via Pagefind with an accessible modal
- SEO-ready: OpenGraph/Twitter, canonical links, and preloaded fonts in [src/components/BaseHead.astro](src/components/BaseHead.astro)
- Themes `light/dark/blue` with persistent toggle; debug toggle for layout borders
- RSS (`/rss.xml`) and sitemap (`/sitemap-index.xml`) generated automatically


## Requerimientos

- Bun

```sh
curl -fsSL https://bun.com/install | bash
```


- Astro @latest
- Tailwdind CSS

## Install & run

```sh
# install dependencies
bun install

# start dev server
bun run dev

# production build
bun run build

# preview the build
bun run preview
```

## Content
- Posts: add `.md` or `.mdx` under `src/content/blog`. Schema validates `title`, `description`, `pubDate`, `updatedDate?`, `heroImage?`, `tags[]`.
- Authors: `src/content/authors.yml`.
- Socials: `src/content/socials.yml`.

Frontmatter example:
```md
---
title: "How we launch in 6 weeks"
description: "End-to-end process for small teams."
pubDate: 2024-12-12
updatedDate: 2025-01-03
tags: [delivery, process]
heroImage: ../../assets/blog/ship.jpg
---
```

## Quick customization
- Site name and description in [src/consts.ts](src/consts.ts).
- Navigation and hero actions in [src/pages/index.astro](src/pages/index.astro).
- Colors, type, and utilities in `src/styles/global.css`.
- Key components: header with search and toggles ([src/components/Header.astro](src/components/Header.astro)), base layout ([src/layouts/BaseLayout.astro](src/layouts/BaseLayout.astro)).