# Project instructions for Claude

Kimberly's personal site: hand-coded static HTML and CSS with no build step, served by GitHub
Pages at `https://mds08011.github.io/kimberlytravel/`. Malcolm maintains it alongside his own
site (`~/projects/mds08011.github.io`), and the two follow the same conventions where they can.
`README.md` has the publishing steps and the folder layout.

- **Root-relative links start with `/kimberlytravel/`**, because this is a project site and
  not the user site. A link to `/style.css` resolves to Malcolm's site, not this one.
- **Page weight.** Pages should load on a slow 2G connection. Photos are resized to 1280 px on
  the long edge at JPEG quality 75 with metadata stripped before they are committed. The
  stylesheet is the local `/kimberlytravel/sakura.css`, never a CDN.
- **The travel map** is an inline SVG in `travelmap/index.html`. The large GeoJSON files in
  `travelmap/` are source data that no live page loads. Don't wire them back into a page.
- **Analytics** are GoatCounter at `ksultz.goatcounter.com`, separate from Malcolm's.
- **Kimberly writes the posts.** Ask Malcolm before publishing or rewriting anything that
  appears under her name.
- **Text encoding.** The 2015 posts were double-encoded once (`â€™` for `’`), which was
  repaired on 2026-11-26. Keep files UTF-8 and keep their existing line endings when editing.
- **Commits** are authored as `mds08011`, with no AI attribution, and wait for Malcolm's OK.
