# Methodology

## Project Approach

The Westport River Watershed Dashboard was developed as a self-directed environmental GIS and data-communication project examining multiple dimensions of watershed condition across the Westport River Watershed in Massachusetts and Rhode Island.

The project combined spatial analysis, environmental monitoring data, cartographic visualization, and web GIS development within a single interactive application.

The overall workflow consisted of:

1. Defining a watershed-scale study area
2. Identifying and acquiring relevant environmental datasets
3. Preparing and integrating spatial and tabular data
4. Conducting watershed-scale environmental analyses
5. Developing maps, statistics, and environmental visualizations
6. Publishing processed data and maps through ArcGIS Online
7. Building an interactive application in ArcGIS Experience Builder
8. Integrating automatically updating environmental information and custom web content

Detailed information about individual datasets and their sources is available in [data_sources.md](docs/data_sources.md).

---

## 1. Study Area & Watershed Framework

The project study area was defined using a **HUC12 watershed boundary from the National Watershed Boundary Dataset (WBD)**.

The selected hydrologic unit spans portions of both Massachusetts and Rhode Island and provided a consistent watershed-scale extent for subsequent environmental analyses.

Rather than constructing a new watershed boundary, the existing HUC12 boundary was used as the geographic framework for integrating environmental information from multiple sources.

Because environmental datasets varied in geographic coverage, subsequent processing depended on the structure of each source. National datasets could often be analyzed continuously across the interstate watershed, while some state-maintained datasets required separate Massachusetts and Rhode Island data to be reconciled and combined.

---

## 2. Data Acquisition & Spatial Preparation

Environmental and geographic datasets were obtained from federal, state, local, nonprofit, and ArcGIS-based data sources.

Data preparation varied by dataset and included techniques such as:

- Reviewing source metadata and geographic coverage
- Organizing spatial and tabular datasets
- Managing coordinate systems and reprojection where required
- Clipping or selecting data to the watershed study area
- Cleaning attribute and tabular information
- Joining related spatial and non-spatial information
- Merging datasets where continuous interstate coverage was required
- Converting or processing spatial features for analysis and visualization
- Applying thematic and unique-value symbology
- Preparing processed layers for publication through ArcGIS Online

Processing decisions were made according to the geographic coverage, format, and intended analytical use of each dataset rather than applying a single standardized workflow to all project data.

---

## 3. Land Cover & Protected Lands Analysis

### Developed Land

Developed-land analysis used **National Land Cover Database (NLCD)** data accessed through ArcGIS Living Atlas.

Because NLCD provides national coverage, a single source could be used across both the Massachusetts and Rhode Island portions of the watershed without requiring separate state datasets.

Land-cover information was processed to isolate developed land-cover classes within the watershed. Intermediate processing converted and prepared developed areas for watershed-scale analysis.

Processed outputs included:

- `nlcd_dev_only`
- `NLCD_Dev_Polygon`
- `Dev_Areas_Westport`

The resulting developed-area dataset was used to calculate watershed-level statistics and create dashboard visualizations communicating the extent of developed land.

### Protected Lands

Protected-land analysis required a different approach because conservation data were maintained separately by Massachusetts and Rhode Island.

Massachusetts protected/open-space data and Rhode Island conservation-land data were prepared and combined to produce continuous protected-land coverage across the interstate watershed.

The integrated dataset included the project output:

- `ProtectedLands_MA_RI_merge`

Additional Rhode Island protected-land polygons were incorporated where necessary to complete coverage.

The resulting data were further processed into `Protected_Areas_Westport` and used to calculate protected-land summary statistics for the dashboard.

This cross-jurisdictional workflow allowed state-specific conservation datasets to be represented within a common watershed-scale analysis.

---

## 4. Water-Quality Data Preparation & Visualization

Published monitoring information from the **Westport River Watershed Alliance (WRWA)** was used to develop the dashboard's water-quality component.

Annual monitoring results were compiled and reorganized into structured tables suitable for analysis and visualization. Supporting Excel datasets were created from the published monitoring information and prepared for use within the ArcGIS environment.

The prepared water-quality data were subsequently incorporated into ArcGIS Online and ArcGIS Experience Builder.

### Multi-Year Monitoring Visualization

Monitoring results from **2022–2024** were organized to allow comparison among seven sampling locations and across monitoring years.

The prepared dataset was used to generate a multi-year line visualization within the ArcGIS web environment, allowing users to compare average coliform bacteria levels spatially and temporally.

### 2025 Water-Quality Indicator

A separate water-quality gauge was developed using **2025 monitoring information** available during the dashboard's development period.

The gauge provided a simplified visual summary of bacteria conditions using clearly labeled water-quality categories.

### Environmental Context

Annual rainfall information for 2022–2024 was presented alongside water-quality results to provide environmental context for observed monitoring patterns.

Summary annotations and statistics were used to help users interpret differences among monitoring years and sampling locations.

The water-quality component was designed to translate monitoring results into an accessible public-facing format while preserving the connection between the underlying environmental measurements and their spatial and temporal context.

The dashboard represents monitoring information incorporated during project development and is not maintained as a continuously updated water-quality monitoring product.

---

## 5. Biodiversity & Species Spotlight

The final biodiversity component of the dashboard was designed around an interactive **Species Spotlight** rather than a conventional habitat-analysis map.

Species and ecological information from the **U.S. Fish and Wildlife Service (USFWS)** was researched and organized into custom digital species cards.

The cards were developed using HTML/CSS and designed to communicate ecological and identification information in an accessible visual format.

The completed cards were integrated into ArcGIS Experience Builder as an interactive component of the larger watershed dashboard.

The Species Spotlight is maintained separately as a supporting project:

[Species Cards Repository](https://github.com/AlyssaPacheco2721/species-cards)

### Exploratory Habitat Analysis

Earlier project development also included exploratory spatial analysis using habitat datasets such as:

- MassGIS BioMap Rare Species Core
- MassGIS NHESP Priority Habitats of Rare Species
- Massachusetts and Rhode Island core-habitat information

Project outputs included habitat summary tables such as:

- `Core_Habitat_Summary`
- `Rare_Species_Core_Summary`
- `Priority_Habitat_Summary`

These analyses were explored during project development but were **not retained as a primary component of the final dashboard**.

The Species Spotlight was ultimately selected as the principal biodiversity communication feature.

---

## 6. Wetlands, Salt Marsh & Sea-Level-Rise Visualization

Wetland and sea-level-rise data were combined to create a coastal vulnerability visualization focused on the spatial relationship between mapped salt-marsh habitat and potential inundation.

### Salt-Marsh Identification

MassDEP wetland polygon data were used to identify mapped salt-marsh areas within the project area.

The source wetlands dataset is a legacy dataset maintained for reference purposes and has since been superseded by newer statewide wetlands mapping. Its use and dataset status are documented in the project's data-source documentation.

### Sea-Level-Rise Scenario

NOAA Sea Level Rise Viewer GeoPackages for Massachusetts and Rhode Island contained multiple sea-level-rise inundation intervals.

Source files included:

- `MA_slr_final_dist.gpkg`
- `RI_slr_final_dist.gpkg`

The **3-foot sea-level-rise scenario** was selected for the dashboard and displayed alongside mapped salt-marsh habitat.

The visualization was intended to communicate the substantial spatial relationship between the selected inundation scenario and existing mapped coastal wetland habitat.

It was designed as an environmental communication tool and **should not be interpreted as a predictive model of future salt-marsh loss or migration**.

---

## 7. Human Impact & Nutrient Pressure

The Human Impact component used watershed information published by the **Westport River Watershed Alliance** to communicate nutrient pressure and its ecological implications.

Published nitrogen concentrations and target values for the Lower East and Lower West Branches were organized into a comparison table.

Differences between current and target conditions were calculated and presented within the dashboard to make nutrient overages easier to interpret.

Supporting graphics and explanatory information connected nutrient loading with the process of eutrophication:

**Runoff and nutrient inputs → increased nutrient availability → algal growth → reduced dissolved oxygen → ecological stress**

The component also incorporated management examples illustrating approaches that can reduce nutrient inputs or support watershed resilience.

This section was designed to connect measured environmental conditions with ecological processes, environmental consequences, and potential management responses.

---

## 8. Watershed Overview & Reference Mapping

A central Watershed Overview map was developed to provide geographic and community context for the project's analytical components.

The map combined ArcGIS Living Atlas reference data, manually compiled local features, and project-derived environmental layers.

Reference information included:

- Rivers and flowlines
- Waterbodies
- Municipal boundaries
- Interstate, major, and local roads
- Beaches
- Fishing and boating access
- Hiking trails
- Bridges, villages, and other landmarks
- WRWA Headquarters

Locally relevant landmarks and recreational-access locations were manually compiled where appropriate, including project layers such as:

- `FishingBoating_Access`
- `Beach_Access_Complete`

Project-derived watershed-boundary and protected-land information was also incorporated into the Overview map.

Layers were organized and symbolized within ArcGIS Pro to create a readable watershed-scale reference map before publication through ArcGIS Online and integration into ArcGIS Experience Builder.

---

## 9. Web GIS Development

Processed spatial layers, environmental datasets, maps, and visualizations were published or incorporated into the ArcGIS web environment.

**ArcGIS Pro** served as the primary environment for spatial data preparation, analysis, and cartographic development.

**ArcGIS Online** was used to host and publish web-accessible project data and maps.

**ArcGIS Experience Builder** was used to assemble the final interactive application and integrate multiple forms of environmental information into a unified interface.

Dashboard components included:

- Interactive watershed mapping
- Developed-land and protected-land statistics
- Multi-year water-quality visualization
- Water-quality indicators
- Species Spotlight cards
- Sea-level-rise and salt-marsh visualization
- Human-impact and nutrient information
- Environmental callout statistics
- Daily environmental conditions

Custom HTML/CSS content was incorporated into Experience Builder for the Species Spotlight component.

The application structure was designed to move beyond individual GIS maps by combining spatial analysis, environmental data, ecological interpretation, and science communication within a single web-based experience.

---

## 10. Daily Conditions & Dynamic Data Integration

The **Daily Conditions** component was developed to provide current environmental context alongside the dashboard's historical and project-period analyses.

### Weather Observations

ArcGIS Living Atlas **Current Weather and Wind Station Data** were used within Experience Builder.

The Living Atlas service is generated from hourly NOAA METAR station observations. Station data, rather than buoy observations, were selected for the dashboard.

Variables displayed included:

- Air temperature
- Wind speed
- Humidity

Individual weather variables were configured within Experience Builder so that the indicators could update as new observations became available from the underlying service.

### Precipitation Forecast

The **National Weather Service 72-Hour Precipitation Forecast** available through ArcGIS Living Atlas was incorporated as an interactive regional map.

The precipitation forecast provides additional environmental context because rainfall and runoff can influence watershed and water-quality conditions.

### Tide Predictions

A station-specific **NOAA Tides & Currents** prediction resource was linked from the Daily Conditions panel.

Rather than manually reproducing tide predictions within the project, users were directed to the NOAA resource for current and upcoming tidal information.

Together, these components allowed the dashboard to combine static and historical environmental analyses with automatically updating observations, forecast information, and external tidal predictions.

---

## Limitations & Design Considerations

Several considerations are important when interpreting the dashboard and its outputs:

- Environmental datasets originated from multiple organizations and were produced for different purposes, geographic extents, and time periods.
- Some analyses required combining independently maintained Massachusetts and Rhode Island datasets to achieve watershed-wide coverage.
- The MassDEP wetlands dataset used for the salt-marsh visualization is a legacy dataset that has since been superseded by newer statewide mapping.
- The 3-foot sea-level-rise component represents the spatial relationship between a selected NOAA inundation scenario and mapped salt-marsh habitat; it is not a predictive ecological model of future marsh loss.
- Water-quality visualizations represent monitoring information incorporated during project development and are not continuously maintained as new annual monitoring data become available.
- Automatically updating Daily Conditions information depends on external ArcGIS, NOAA, and National Weather Service data services.
- Reference and communication components were designed for watershed-scale interpretation and public engagement rather than site-specific regulatory or engineering analysis.

---

## Software & Technologies

The project workflow incorporated:

- **ArcGIS Pro** — spatial analysis, geoprocessing, data preparation, and cartography
- **ArcGIS Online** — web GIS publishing and hosted project data
- **ArcGIS Experience Builder** — interactive application development
- **ArcGIS Living Atlas** — reference and dynamic environmental services
- **Microsoft Excel** — environmental data cleaning, organization, and preparation
- **QGIS** — supporting GIS preparation and visualization
- **HTML/CSS** — custom interactive Species Spotlight components

---

## Supporting Documentation

- [Data Sources](docs/data_sources.md) — detailed dataset provenance, source information, and project use
- [Westport River Watershed Dashboard Project](https://alyssapacheco.webflow.io/work/westport-dashboard)
- [Species Cards Repository](https://github.com/AlyssaPacheco2721/species-cards)
