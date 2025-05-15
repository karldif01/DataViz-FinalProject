# User Manual for COVID-19 Data Visualization Project
# Karl Hu Josefsson

## Prerequisites
- Web Browser
  Recommendations: Chrome, Firefox, Safari, or Edge
- Local HTTP Server  
  Browsers block HTTP requests (e.g., `fetch`) on `file://`. Use:
  - **Python 3.8+**: `python3 -m http.server 8000`
- **Internet Connection**  
  Required for fetching external data via URLs.

## Project Dependencies
This is a **static** HTML/CSS/JS project, so no build step required. All libraries are loaded via CDN:

- D3.js v7.0
  ```html
  <script src="https://d3js.org/d3.v7.min.js"></script>
  ```
- GeoJSON (countries)
  Fetched from:
  `https://raw.githubusercontent.com/johan/world.geo.json/master/countries.geo.json`

## Running Locally
1. Open a terminal and `cd` into `/your-folder/`.
2. Start a server:
     python3 -m http.server 8000

3. In your browser, visit `http://localhost:8000/index.html`.

## Start Project
- Enter this URL in your browser:
  https://karldif01.github.io/DataViz-FinalProject/

## Data Sources
Data is fetched live via D3’s `d3.csv`.

- Hospital Occupancy 
  /data/scandinavia_hospitalizations_per10M.csv
- Mortality (deaths per 10M)
  /data/scnadinavia_deaths_per_10m.csv
- Animated Scatter (deaths time series)
  /data/scandinavia_deaths_per_10m.csv
- Choropleth Map (cases) 
  /data/total_cases.csv
- GDP
  /data/gdp-data.csv
- Unemployment
  /data/unemployment.csv

## Interactions & Shortcuts
- **Line Charts**: hover for tooltips showing exact values.
- **Legend Hover**: hover legend items (e.g., “Sweden”) to highlight that country.
- **Combined Hospital Chart**: hover to see vertical guide line and country dots.
- **Animated Scatterplot**:
  - Play/Pause button toggles animation.
  - Slider lets you scrub to any date.
- **Treemap**: hover cells for country and value.
- **Choropleth Map**:
  - Slider for date selection updates map.
  - Hover polygons for tooltip details.

## Troubleshooting
- Empty charts / CORS errors: ensure you're running over HTTP (`localhost:8000`).
- Missing background picture: ensure `background2.png` is in the project folder and is referenced in the CSS styling.

