# Kimberly Sultz - Personal Website

Welcome to the source repository for Kimberly Sultz's personal website. This is a static HTML/CSS site emphasizing semantic structure and zero bloat.

## Publishing SOP

To maintain the site's simplicity, all updates are made manually using basic HTML files. Follow these standard operating procedures to publish new content:

### Directory Organization

Content is categorized into three primary folders:

- `/aquatics/`: For all YMCA, Aquatics Director, and Operational (SOP) content.
- `/crafts/`: For knitting, crafting, and hobby-related posts.
- `/travel/`: For travel logs, interactive map files, and trip summaries.

### Creating a New Post / Page

1. **Copy the Template**: Duplicate the `boilerplate.html` file into the appropriate directory (e.g., `/aquatics/new-sop.html`).
2. **Update Meta Information**: Update the `<title>` tag and the `<h1>` to reflect the new content.
3. **Write Content**: Fill in the `<main>` tag with standard HTML elements (`<p>`, `<ul>`, `<table>`). Use the `<details>` and `<summary>` tags for collapsable content like lengthy SOPs.
4. **Link to Root**: Once the page is complete, add a list item with a link to this new file in the appropriate section of `/index.html` (e.g., under "Latest in Aquatics & Ops").

### Updating the Interactive Travel Map

The travel map utilizes GeoJSON for markers and routes.

1. **Update GeoJSON Data**: Add new coordinate features to the primary `KS_Map.geojson` file located in the repository.
2. **Commit Changes**: Push the updated `.geojson` file to the `master` branch. The web map fetches the raw file directly.
3. **Map Framework**: The map uses Leaflet/Mapbox with Bootstrap for a responsive template. No rebuild step is necessary—simply update the data file.

---

### Additional Map Documentation

Based on: https://github.com/bmcbride/geojson-share-maps

- **Web Map**: https://mds08011.github.io/KimberlyTravel/?src=https://raw.githubusercontent.com/mds08011/KimberlyTravels/master/KS_Map.geojson
- **Raw geojson**: https://raw.githubusercontent.com/mds08011/KimberlyTravel/master/KS_Map.geojson
- **States**: https://mds08011.github.io/KimberlyTravel/?src=https://raw.githubusercontent.com/mds08011/KimberlyTravels/master/source-data/geojson/ne_10m_admin_1_states_provinces/KS_States.geojson

**Features:**
- Fullscreen mobile-friendly map template with responsive navbar and modal popups
- Built on Bootstrap and Leaflet/Mapbox frameworks
- Supports GeoJSON feature styling via simplestyle-spec

### Other Resources

- Format and convert: https://app.placemark.io/converter
- Validate geojson files: http://geojsonlint.com/
- Visualize and edit geojson: https://geojson.io
- Download source SHP: http://www.naturalearthdata.com/