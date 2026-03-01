# 🇮🇳 India — Literacy & Sanitation Interactive Choropleth Map

An interactive choropleth map of India built with **Python**, **Folium**, and **GeoPandas** that visualizes state-level **Total Literacy (%)** and **Basic Sanitation (%)** data. Users can toggle between layers and hover over states to view detailed statistics.

---

## 📸 Features

- **Dual Choropleth Layers** — switch between:
  - **Basic Sanitation (%)** — `YlGnBu` color palette (shown by default)
  - **Total Literacy (%)** — `YlOrRd` color palette
- **Layer Control** — toggle layers on/off from the top-right corner of the map
- **Interactive Tooltips** — hover over any state/UT to see:
  - State name
  - Total Literacy (%)
  - Basic Sanitation (%)
- **Highlight on Hover** — states highlight when hovered
- **Light Basemap** — clean CartoDB Positron tiles for readability

---

## 📁 Project Structure

```
minor/
├── DATA/
│   ├── final_result.csv        # Merged literacy + sanitation data by State/UT
│   ├── lit.csv                 # Raw literacy data
│   ├── san.csv                 # Raw sanitation data
│   ├── SDG6.csv                # SDG 6 (Water & Sanitation) data
│   ├── men.csv                 # Gender-wise data (men)
│   ├── women.csv               # Gender-wise data (women)
│   ├── literacy.ipynb          # Notebook for literacy data processing
│   └── sdg_6.ipynb             # Notebook for SDG 6 data processing
│
├── GEOJASON/
│   ├── india.geojson           # GeoJSON with Indian state/district boundaries
│   ├── map.ipynb               # Main notebook — generates the interactive map
│   └── maping.ipynb            # Older version of the mapping notebook
│
├── MAP/
│   └── index.html              # Exported standalone HTML map
│
├── Nootbook/
│   └── comparison.ipynb        # Notebook for data comparison/analysis
│
├── OUTPUT/                     # Output files directory
│
└── README.md                   # This file
```

---

## 🛠️ Tech Stack

| Tool        | Purpose                                   |
|-------------|-------------------------------------------|
| Python 3    | Core programming language                 |
| Pandas      | Data loading and manipulation             |
| GeoPandas   | Geospatial data handling and merging      |
| Folium      | Interactive map generation (Leaflet.js)   |
| Jupyter     | Notebook environment for development      |

---

## 🚀 Getting Started

### Prerequisites

Make sure you have Python 3 installed with the following packages:

```bash
pip install pandas geopandas folium jupyter
```

### Running the Map

1. Open the notebook:
   ```bash
   cd GEOJASON
   jupyter notebook map.ipynb
   ```

2. **Run all cells** (`Kernel → Restart & Run All`)

3. The interactive map will render in the last cell output.

4. Use the **layer control** (top-right corner) to toggle between:
   - Basic Sanitation (%)
   - Total Literacy (%)

---

## 📊 Data Sources

- **Literacy Data** — State/UT-wise total literacy rates
- **Sanitation Data** — Percentage of population with basic sanitation services (SDG 6 indicator)
- **GeoJSON** — District-level boundaries of India (2011 Census)

---

## 📌 Notes

- State name mismatches between CSV data and GeoJSON (e.g., `Jammu & Kashmir` vs `Jammu and Kashmir`) are handled automatically in the notebook.
- The GeoJSON contains **district-level** boundaries, while the CSV data is at the **state/UT level** — the merge maps state-level data to all districts within each state.
- The exported HTML map can be found in `MAP/index.html` and viewed directly in a browser without Python.

---

## 📄 License

This project is for academic/educational purposes (Minor Project).
