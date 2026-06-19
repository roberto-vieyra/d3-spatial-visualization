# Spatial Data Visualization: Socio-Economic Heatmaps (D3.js)

A frontend data visualization architecture designed to translate multidimensional statistical tabulations into interactive geospatial narratives. 

##  Project Context
While statistical models (e.g., Small Area Estimation) provide rigorous variance stabilization, communicating these results to institutional decision-makers requires intuitive, high-resolution spatial interfaces. This project renders complex socio-economic indicators (e.g., labor informality, demographic shifts) across regional boundaries using SVG-based cartography.

##  Architecture & Technical Decisions
- **Rendering Engine:** Utilized **D3.js (Data-Driven Documents)** to bind tabular socio-economic data to the Document Object Model (DOM), allowing for dynamic SVG generation.
- **Geospatial Optimization:** Implemented **TopoJSON** over standard GeoJSON to encode topology. This eliminated redundancy in shared regional borders, significantly reducing the file size of the map geometries for faster web loading.
- **Editorial Export:** Configured the layout to ensure high-resolution SVG/Canvas exports, enabling the transition from interactive web exploration to static institutional reports.

##  Tech Stack
- **Libraries:** `D3.js (v7)`, `TopoJSON Client`
- **Languages:** JavaScript (ES6), HTML5, CSS3
- **Data Structures:** TopoJSON, CSV/JSON (Analytical Outputs)

## Visual Evidence
*(Check the `/docs` folder for high-resolution exports of the generated thematic maps).*

## Local Execution
To view the interactive maps locally, bypass CORS restrictions by running a local Python server:
```bash
git clone [https://github.com/TU_USUARIO/d3-spatial-visualization.git](https://github.com/TU_USUARIO/d3-spatial-visualization.git)
cd d3-spatial-visualization
python -m http.server 8000
