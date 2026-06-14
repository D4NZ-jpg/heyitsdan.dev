# heyitsdan.dev

My personal site. One small page, built with Astro and hosted on Cloudflare Pages.

It's live at https://heyitsdan.dev.

## What's in here

It's a static Astro site. The styling is plain CSS with a warm light theme, and Tailwind v4 is set up in case I want it later. The fonts (Fraunces, Plus Jakarta Sans, JetBrains Mono) are self-hosted with Fontsource, so nothing loads from Google.

## Running it

You'll need Node 22.12+ and pnpm.

```sh
pnpm install
pnpm dev
```

The dev server runs at http://localhost:4321.

`pnpm build` writes the static site to `dist/`, and `pnpm preview` serves that build.

## Deploying

It's on Cloudflare Pages with these settings:

- Framework preset: Astro
- Build command: `pnpm build`
- Output directory: `dist`
- `NODE_VERSION=22.12`

Everything is static, so there's no adapter or server runtime. If `pnpm install` ever complains about ignored build scripts, the approvals for esbuild and sharp live in `pnpm-workspace.yaml`.

## Files

```text
public/favicon.svg     the wave
src/pages/index.astro  the page and its inline script
src/styles/global.css  tokens, theme, font imports
astro.config.mjs       site URL and the Tailwind plugin
```
