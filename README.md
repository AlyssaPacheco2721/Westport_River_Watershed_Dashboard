# Westport River Watershed Dashboard

**Environmental GIS Analysis & Interactive Data Visualization**

An interactive environmental GIS project integrating spatial, ecological, water-quality, land-cover, climate, and near-real-time environmental data to explore conditions across the **Westport River Watershed in Massachusetts and Rhode Island**.

The project combines federal, state, local, and nonprofit environmental datasets within a watershed-scale framework. GIS processing, environmental data analysis, cartographic visualization, and web GIS development were used to examine watershed conditions and translate environmental information into an accessible interactive dashboard.

---

## Project Overview

The Westport River Watershed Dashboard was developed as a self-directed environmental GIS and data-communication project focused on bringing multiple dimensions of watershed health into one interactive platform.

The project integrates national datasets with Massachusetts and Rhode Island environmental data, local watershed-monitoring information, and automatically updating environmental services.

Major components include:

- HUC12 watershed-scale spatial analysis
- Developed-land and protected-land analysis
- Cross-jurisdictional GIS data integration
- Multi-year water-quality analysis and visualization
- Interactive biodiversity and species information
- Sea-level-rise and salt-marsh vulnerability visualization
- Nutrient-pressure and human-impact communication
- Current weather, precipitation, and tidal information
- Interactive watershed reference mapping
- Web GIS development and environmental data communication

---

## Technical Workflow

### 1. Watershed Boundary & Cross-Jurisdictional Data Integration

A HUC12 watershed boundary from the **National Watershed Boundary Dataset (WBD)** was used to define the Westport River Watershed study area spanning Massachusetts and Rhode Island.

While the watershed boundary provided a unified hydrologic study area, some environmental datasets were maintained separately by Massachusetts and Rhode Island agencies. Subsequent analyses therefore required identifying comparable datasets across jurisdictions and integrating them where necessary to represent conditions across the complete watershed.

This work involved multi-source data acquisition, spatial data preparation, coordinate-system management, attribute processing, and integration of environmental datasets within a common GIS environment.

### 2. Land Cover & Protected Lands Analysis

Developed land and protected land were evaluated using separate spatial datasets and processing workflows.

**National Land Cover Database (NLCD)** data provided consistent national coverage across both Massachusetts and Rhode Island and were processed to isolate developed land within the watershed.

Protected-land analysis required additional cross-jurisdictional processing. Massachusetts protected/open-space data were combined with Rhode Island conservation-land data to create a unified protected-lands dataset for the interstate watershed.

The resulting developed-area and protected-land layers were used to calculate watershed-level summary statistics and create thematic dashboard visualizations.

### 3. Water-Quality Analysis & Visualization

Published **Westport River Watershed Alliance (WRWA)** monitoring results were compiled, cleaned, reorganized, and prepared for analysis and web visualization.

The water-quality component includes:

- A multi-year line chart comparing average coliform bacteria levels across seven monitoring locations from **2022–2024**
- A **2025 water-quality gauge** summarizing monitoring conditions
- Annual rainfall context for interpreting water-quality patterns
- Summary statistics and annotations communicating bacteria exceedance patterns
- Interactive visualization of spatial and temporal differences in monitoring results

Prepared water-quality data were incorporated into ArcGIS Online and used within ArcGIS Experience Builder to translate monitoring results into an accessible public-facing format.

### 4. Habitat & Biodiversity — Species Spotlight

The final biodiversity component focuses on an interactive **Species Spotlight** highlighting organisms associated with the Westport River Watershed and surrounding coastal ecosystem.

Species and ecological information from the **U.S. Fish and Wildlife Service (USFWS)** was researched and translated into custom digital species cards.

The cards were developed using HTML/CSS and integrated into ArcGIS Experience Builder to combine ecological information with interactive environmental communication.

### 5. Wetlands, Salt Marsh & Sea-Level Rise

MassDEP wetland data were used to identify mapped salt-marsh habitat, while **NOAA Sea Level Rise Viewer** data provided inundation scenarios for Massachusetts and Rhode Island.

A **3-foot sea-level-rise scenario** was selected and displayed alongside mapped salt-marsh areas to visualize their spatial relationship and communicate potential coastal exposure.

This component was designed as an environmental communication visualization rather than a predictive model of future marsh loss.

### 6. Human Impact & Nutrient Pressure

Information from the **Westport River Watershed Alliance** was used to communicate nutrient pressure within the watershed.

Current and target nitrogen concentrations for the Lower East and Lower West Branches were compared to show conditions relative to watershed targets. Supporting visual communication connected nutrient loading with eutrophication processes, including runoff, algal growth, and reduced dissolved oxygen.

The component also presented examples of watershed-management approaches and connected nutrient pressure with broader coastal vulnerabilities.

### 7. Watershed Overview & Reference Mapping

A central interactive map combines analytical outputs with supporting geographic and community reference information.

Mapped features include:

- Rivers and waterbodies
- Municipal boundaries
- Interstate, major, and local roads
- Beaches and recreational access
- Fishing and boating access
- Hiking trails
- Local landmarks
- WRWA Headquarters
- Protected lands
- Westport River Watershed boundary

Reference information was assembled using ArcGIS Living Atlas and manually compiled local project features, while analytical layers were derived from datasets documented elsewhere in the project.

### 8. Daily Environmental Conditions

The dashboard's **Daily Conditions** component supplements historical and project-period analysis with automatically updating environmental information.

ArcGIS Living Atlas services derived from **NOAA METAR station observations** provide current:

- Air temperature
- Wind speed
- Humidity

The dashboard also incorporates:

- **National Weather Service 72-Hour Precipitation Forecast**
- **NOAA tide predictions**

These services were integrated through ArcGIS Experience Builder to provide current environmental context without requiring manual updates to the dashboard.

---

## GIS & Data Processing

The project involved a range of GIS, environmental data-management, and web GIS techniques, including:

- Multi-source environmental data acquisition
- Data cleaning and organization
- Attribute and tabular joins
- Cross-jurisdictional spatial data integration
- Coordinate-system management and reprojection where required
- Spatial clipping and polygon processing
- Land-cover classification and developed-area extraction
- Protected-land dataset integration
- Summary-statistic calculations
- Environmental monitoring-data preparation
- Thematic and unique-value symbology
- Cartographic design
- ArcGIS Online data publishing
- Hosted environmental data integration
- ArcGIS Living Atlas integration
- Interactive web GIS development
- HTML/CSS integration within Experience Builder
- Environmental data visualization and science communication

---

## Tools & Technologies

- **ArcGIS Pro** — spatial data preparation, analysis, geoprocessing, and cartography
- **ArcGIS Online** — web GIS hosting and environmental data publishing
- **ArcGIS Experience Builder** — interactive dashboard and web application development
- **ArcGIS Living Atlas** — environmental and geographic reference services
- **QGIS** — supporting GIS data preparation and visualization
- **Microsoft Excel** — environmental data cleaning, organization, and preparation
- **HTML/CSS** — custom interactive Species Spotlight components

---

## Data Sources

The project integrates environmental and geospatial information from multiple authoritative sources, including:

- **National Watershed Boundary Dataset (WBD)** — HUC12 watershed boundary
- **National Land Cover Database (NLCD)** — developed-land analysis
- **MassGIS / MassDEP** — protected lands and wetlands
- **Rhode Island conservation datasets** — protected-land coverage
- **NOAA** — sea-level-rise inundation, METAR weather observations, and tide predictions
- **National Weather Service (NWS)** — precipitation forecasts
- **U.S. Fish and Wildlife Service (USFWS)** — Species Spotlight ecological information
- **Westport River Watershed Alliance (WRWA)** — water-quality monitoring and watershed nutrient information
- **ArcGIS Living Atlas** — environmental services and supporting geographic reference layers

For dataset-level provenance, geographic coverage, project use, processing notes, and source links, see:

➡️ **[Detailed Data Sources & Documentation](docs/data-sources.md)**

---

## Related Project: Watershed Species Cards

The dashboard's Species Spotlight includes a collection of custom interactive species cards designed to communicate ecological information about organisms associated with the Westport River Watershed and surrounding coastal ecosystem.

The cards were developed separately using HTML/CSS and incorporated into the larger dashboard through ArcGIS Experience Builder.

➡️ **[View the Species Cards Repository](https://github.com/AlyssaPacheco2721/species-cards)**

---

## Project Presentation

A visual overview of the completed dashboard and its major environmental components is available here:

➡️ **[View the Westport River Watershed Dashboard Project](https://alyssapacheco.webflow.io/work/westport-dashboard)**

---

## Skills Demonstrated

`Environmental GIS` `Spatial Analysis` `Watershed Science` `Environmental Data Analysis` `Water Quality` `Land Cover Analysis` `Coastal GIS` `Cross-Jurisdictional Data Integration` `Climate Vulnerability` `ArcGIS Pro` `ArcGIS Online` `ArcGIS Experience Builder` `ArcGIS Living Atlas` `QGIS` `Data Visualization` `HTML/CSS` `Science Communication`

---

## Author

**Alyssa Pacheco**  
Environmental Scientist | GIS & Coastal Science
