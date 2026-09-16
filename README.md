# studiofelvar.com

Static one-page site. No build step.

## Deploy — Cloudflare Workers (static assets)
1. Push this folder's contents to `Ehnrik/studiofelvar` (branch `main`), including `wrangler.toml`.
2. Cloudflare → Create an app → Connect to Git → pick the repo.
3. Build command: *(leave empty)*. Deploy command: `npx wrangler deploy`.
4. Deploy, then Settings → Domains & Routes → add `studiofelvar.com` and `www.studiofelvar.com`.

`wrangler.toml` is what makes this work — it tells Wrangler the repo root is a static asset
directory, so there is nothing to build.

Standalone Pages projects are no longer offered on new Cloudflare accounts — Workers with
static assets is the equivalent, and `wrangler.toml` is what makes it work with no build step.

## Cutting over from Cargo
Cloudflare Pages gives you a `*.pages.dev` URL immediately — check that first. Only repoint the
`studiofelvar.com` DNS records away from Cargo once you're happy with it.

## Files
- `index.html` — the whole site (inline styles, one inline script)
- `assets/` — series artwork
- `robots.txt`, `sitemap.xml`

## Still to do
- Replace Archivo with Articulat CF: upload the woff2 files to `assets/fonts/`, swap the Google
  Fonts `<link>` for an `@font-face` block, change `font-family: Archivo` to `Articulat CF`.
- Videos for Sportzentrum Oerlikon and Do You Accept Cookies? — those two entries currently show
  striped placeholders and a dummy waveform player.
