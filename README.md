# studiofelvar.com

Static one-page site. No build step — Cloudflare serves these files as-is.

## Update the live site
1. Replace the repo contents with this folder's contents (keep the same structure).
2. Commit to `main`.
3. Cloudflare redeploys automatically; check the Worker's Deployments tab.
4. Hard-reload the site (Cmd+Shift+R) — the old version caches.

## Files
- `index.html` — the whole site (inline styles, one inline script)
- `favicon.svg` — F monogram
- `wrangler.toml` — tells Cloudflare the repo root is a static asset directory
- `assets/` — artwork and the awards photo
- `robots.txt`, `sitemap.xml`

## Still to do
- Videos for Sportzentrum Oerlikon and Do You Accept Cookies? — both entries show striped
  16:9 placeholders sized for the real footage. Export ~720p H.264 under 25 MB (Cloudflare's
  per-file limit), drop into `assets/`, and the placeholder swaps for a `<video>` element.
- Articulat CF: upload woff2 files to `assets/fonts/`, replace the Google Fonts `<link>`
  with an `@font-face` block, change `font-family: Archivo` to `Articulat CF`.
- No Open Graph image yet — a 1200x630 `assets/og.jpg` would give shared links a preview.
