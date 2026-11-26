# Kimberly Sultz - Personal Website

Welcome to the source repository for Kimberly Sultz's personal website. This is a static HTML/CSS site emphasizing semantic structure and zero bloat.

## Publishing SOP

To maintain the site's simplicity, all updates are made manually using basic HTML files. Follow these standard operating procedures to publish new content:

### Directory Organization

- `/blog/<YYYY-MM-DD>/`: one folder per post, with the post's photos beside it. The 2015 posts are from Peace Corps Mali. The 2026 posts each describe one of the tools.
- `/blog/img/`: screenshots used by the 2026 tool posts.
- `/tools/`: single-file tools (aquatics, knitting and crafts), listed on `/tools/index.html`.
- `/travelmap/`: the travel map.
- `cocktails.html`, `about.html`: standalone pages.

The site is served from `https://mds08011.github.io/kimberlytravel/`, so root-relative links start with `/kimberlytravel/`.

### Creating a New Post / Page

1. **Copy the Template**: Duplicate `boilerplate.html` into a new dated folder under `/blog/`.
2. **Update Meta Information**: Update the `<title>` tag and the `<h1>` to reflect the new content.
3. **Write Content**: Fill in the `<main>` tag with standard HTML elements (`<p>`, `<ul>`, `<table>`). Use the `<details>` and `<summary>` tags for collapsible content like lengthy SOPs.
4. **Photos**: Resize to 1280 px on the long edge at JPEG quality 75 and strip the metadata before committing, so the page loads on a slow connection.
5. **Link It**: Add the post to `/blog/index.html`.

The stylesheet is a local copy of sakura.css v1.5.1 at `/kimberlytravel/sakura.css` (MIT, by oxalorg), plus each page's `style.css`.

### The Travel Map

`/travelmap/index.html` is a self-contained inline SVG world map, generated from `world-atlas-countries.geojson` in an equirectangular projection. It loads no tiles, libraries or external data. To change which places are shaded, edit the SVG in that page.

The large GeoJSON files in `/travelmap/` (`kgs-world.geojson`, `world-atlas-countries.geojson`, `us-atlas-states.geojson`) are source data and are not loaded by the live page. The `leaflet-map-*` folders are the older Leaflet templates, based on https://github.com/bmcbride/geojson-share-maps.

### Other Resources

- Format and convert: https://app.placemark.io/converter
- Validate geojson files: http://geojsonlint.com/
- Visualize and edit geojson: https://geojson.io
- Download source SHP: http://www.naturalearthdata.com/