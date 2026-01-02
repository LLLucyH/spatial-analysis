# 🏙️ Strategic Analysis of Toronto Parks & Recreation Program Distribution

## 📌 Project Overview
This project analyzes the geographic and socio-economic distribution of **Toronto Parks & Recreation programs**, with a focus on **child-focused services (ages 0–14)** and **equity across neighbourhoods**.

Using demographic, geospatial, and program-level data from Toronto’s Open Data portal, the analysis evaluates whether programs are:
1. Strategically aligned with **demographic demand**, and  
2. Equitably distributed across **Neighbourhood Improvement Areas (NIAs)** and low-income communities.

The findings reveal that while program allocation is broadly equitable on a per-capita basis, it is **not strategically optimized** to serve child-dense neighbourhoods or communities facing greater barriers.

---

## 🔍 Key Research Questions
- Are child-focused programs aligned with the geographic concentration of children?
- Do neighbourhoods with higher child populations receive more programs or greater activity diversity?
- Are Parks & Recreation programs disproportionately allocated to or away from NIAs and low-income areas?
- Does equity exist in practice, or only in per-capita allocation?

---

## 📊 Key Findings
- **Near-zero correlation** between child population share and:
  - Number of child programs  
  - Total child program sessions  
  - Activity diversity  
- **34 neighbourhoods** identified as underserved (high child population, low program availability)
- Program distribution across NIAs and non-NIAs shows **no statistically significant difference** (ANOVA p > 0.2)
- Equity exists at a **baseline level**, but allocation is **not needs-based or demand-driven**

---

## 🗺️ Data Sources
All data were obtained programmatically from **Toronto Open Data (CKAN API)**:
- Parks & Recreation registered programs
- Drop-in programs
- Neighbourhood Profiles (demographics, income, age)
- Municipal address points
- Neighbourhood boundary shapefiles

---

## 🛠️ Methods & Techniques

### Data Engineering
- CKAN API ingestion for reproducible data access
- Data cleaning and normalization using `pandas`
- Address standardization and geocoding
- Session count derivation from program date ranges

### Geospatial Analysis
- Spatial joins between program locations and neighbourhood boundaries
- Coordinate reprojection (EPSG:4326 → EPSG:32617) for accurate density calculations
- Program aggregation at neighbourhood and address levels

### Statistical Analysis
- Pearson correlation analysis
- ANOVA tests for neighbourhood equity comparison
- Per-capita and low-income–weighted program density metrics

---

## 📈 Visualizations
The project includes:
- Choropleth maps of child population share and program supply
- Scatter plots identifying underserved neighbourhoods
- Correlation heatmaps
- Violin plots comparing program density across neighbourhood types
- Multi-layer geospatial maps (population density, income, NIA status)

All figures are saved to the `figures/` directory as high-resolution PDFs.

---
