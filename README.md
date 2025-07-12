# 🍇 Vineyard Site Selection Analysis in Central Otago (GIS Project)

This GIS project analyzes vineyard site suitability in Central Otago, New Zealand — one of the world’s southernmost wine regions. Using spatial data and regression models, we identified and quantified the geographic factors influencing vineyard distribution across six sub-regions.

---

## 🎯 Objectives

- Digitize and classify vineyard areas in Central Otago.
- Analyze 8 environmental factors (slope, soil type, elevation, aspect, precipitation, etc.).
- Apply OLS and GWR models to identify both global and localized influences.
- Generate spatial insights and suitability maps to support vineyard planning.

---

## 🧰 Tools & Techniques

- **Software**: ArcGIS Pro
- **Methods**: Zonal Statistics, OLS Regression, Geographically Weighted Regression (GWR)
- **Key Factors**: Slope, Soil Type, Aspect, Elevation, Precipitation, Temperature, Distance to Water, Soil Temperature (January)

---

## 🧪 Analysis Workflow

1. **Study Area and Sub-Region Digitization**  
   Mapped vineyard boundaries across Central Otago and categorized them into 6 key sub-regions using aerial imagery and administrative boundaries.

2. **Geographic Factor Extraction**  
   Selected 8 environmental factors (e.g., slope, temperature, precipitation) and calculated Zonal Statistics per vineyard polygon.

3. **Statistical Modeling**  
   Applied OLS regression to evaluate global relationships and Geographically Weighted Regression (GWR) to identify spatially varying influences across sub-regions.

4. **Visualization and Interpretation**  
   Created suitability maps and residual plots to compare model performance and generate practical insights for vineyard planning.

### 📌 Workflow Diagram

**Digitizing and Creating Sub-Regions in Central Otago Vineyards**
![Analysis Workflow 1 ](./Workflow%20Diagram/Digitizing%20and%20Creating%20Sub-Regions%20in%20Central%20Otago%20Vineyards.jpg)

**Vineyards Factor Analysis in Central Otago**
![Analysis Workflow 2 ](./Workflow%20Diagram/Vineyards%20Factor%20Analysis%20in%20Central%20Otago.jpg)

---

## 📁 Repository Structure

- `m1 study area/` — Maps and shapefiles defining the Central Otago study region and its six sub-regions.
- `m2 factors/` — Factor-specific distribution maps (e.g., slope, precipitation, soil type).
- `m3 OLS+GWR/` — Results from OLS and GWR models, including residual distribution maps.
- `ANALYZING VINEYARD SITE SELECTION IN CENTRAL OTAGO.pdf` — Final report with full methodology, analysis, and discussion.

---

## 🗺️ Sample Maps

> You can embed key visuals here using Markdown:

### Study Area Overview

![Study Area](./m1%20study%20area/StudyareaOverrall.jpg)

### Example: Soil Type Distribution

![Distance to Water](./m2%20factors/N3-water.jpg)

### GWR Residual Map

![GWR Residual](./m3%20OLS+GWR/GWRWithNonVineyard.jpg)

---

## 📊 Key Insights

- **OLS Results**: Distance to water, precipitation, slope, and soil type are significant at the regional level.
- **GWR Results**: Factor influences vary by sub-region; January soil temperature is critical in some zones.
- **Model Fit**: GWR achieved higher explanatory power (Adjusted R² = 0.27) than OLS, highlighting the importance of spatial heterogeneity.

---

## 🌐 Data Sources

| Data                                                 | Feature Class                 | Type    | Source                                                                                                       |
| ---------------------------------------------------- | ----------------------------- | ------- | ------------------------------------------------------------------------------------------------------------ |
| NZ Vineyard Polygons (Topo, 1:50k)                   | Digitized Vineyards           | Polygon | [Link](https://data.linz.govt.nz/layer/50367-nz-vineyard-polygons-topo-150k/)                                |
| Otago 0.3m Rural Aerial Photos                       |                               | Raster  | [Link](https://data.linz.govt.nz/layer/106403-otago-03m-rural-aerial-photos-2019-2021/)                      |
| Queenstown Lakes 0.1m Urban Aerial Photos            |                               | Raster  | [Link](https://data.linz.govt.nz/layer/112781-queenstown-lakes-01m-urban-aerial-photos-2022-2023/)           |
| NZ Lake Polygons (Topo, 1:50k)                       | Distance to Water             | Polygon | [Link](https://data.linz.govt.nz/layer/50293-nz-lake-polygons-topo-150k/)                                    |
| NZ River Polygons (Topo, 1:50k)                      |                               | Polygon | [Link](https://koordinates.com/from/data.linz.govt.nz/layer/50328-nz-river-polygons-topo-150k/)              |
| Soil Temperature (January)                           | January Soil Temperature      | Raster  | _Lincoln Uni Local Dataset_ `J:\NZClimateGridsTM\SoilTemperature`                                            |
| NZEnvDS_Total Annual Precipitation                   | Precipitation                 | Grid    | [Link](https://koordinates.com/from/lris.scinfo.org.nz/layer/105725-nzenvds-total-annual-precipitation-v10/) |
| LENZ – Mean Minimum Temperature of the Coldest Month | Min_Temperature_Coldest Month | Grid    | [Link](https://lris.scinfo.org.nz/layer/48092-lenz-mean-minimum-temperature-of-the-coldest-month/)           |
| NZDEM South Island 25 metre                          | Aspect / Slope / Elevation    | Grid    | [Link](https://koordinates.com/from/lris.scinfo.org.nz/layer/48127-nzdem-south-island-25-metre/)             |
| FSL New Zealand Soil Classification v1.1             | Soil Type                     | Polygon | [Link](https://lris.scinfo.org.nz/layer/112060-fsl-new-zealand-soil-classification-v11/)                     |
