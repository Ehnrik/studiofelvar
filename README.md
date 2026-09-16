# studiofelvar.com

Static one-page site. No build step.

## Deploy — Cloudflare Pages
1. Push this folder's contents to `Ehnrik/studiofelvar` (branch `main`).
2. Cloudflare dashboard → Workers & Pages → Create → Pages → Connect to Git → pick the repo.
3. Framework preset: **None**. Build command: *(leave empty)*. Build output directory: `/`.
4. Deploy. Then Custom domains → Set up a domain → `studiofelvar.com` and `www.studiofelvar.com`.

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
