# Data Sources

## Overview

This project integrates environmental and geospatial datasets from
Massachusetts and Rhode Island to support watershed-scale analysis
of land use, habitat, water quality, climate vulnerability, and
human use within the Westport River Watershed.

## Watershed Boundary

### National Watershed Boundary Dataset (WBD) — HUC12 Subwatersheds

**Source:** National Watershed Boundary Dataset (WBD), accessed through MassGIS  
**Data Type:** Shapefile  
**Hydrologic Unit:** HUC12 (12-digit Hydrologic Unit Code)  
**Geographic Coverage:** Massachusetts and Rhode Island  
**Purpose:** Definition of the Westport River Watershed study area.

**Project Use:**  
HUC12 watershed boundary data were used as the hydrologic foundation for the project study area. The selected watershed boundary spans portions of Massachusetts and Rhode Island, as identified within the source dataset, and served as the common spatial extent for subsequent land-use, habitat, water-quality, and climate analyses.

**Processing Notes:**  
The watershed boundary was carried forward from an earlier Westport River land-cover analysis and reused as the study boundary for the larger dashboard project. Subsequent environmental datasets were prepared according to their geographic coverage, including cross-jurisdictional integration of Massachusetts and Rhode Island datasets where necessary to support analysis across the complete watershed extent.

---
## Overview & Reference Layers

### Watershed Overview Map

**Sources:** ArcGIS Living Atlas and manually compiled project features  
**Data Type:** Hydrography, transportation, administrative boundaries, recreational access, landmarks, and environmental reference layers  
**Geographic Coverage:** Westport River Watershed and surrounding area  
**Purpose:** Provide geographic and community context through the dashboard's central interactive watershed map.

**Project Use:**  
The Watershed Overview map combines environmental analysis outputs with supporting geographic and community reference layers. These datasets provide spatial context for interpreting watershed conditions and allow users to explore waterways, transportation networks, municipalities, recreational access, landmarks, and protected areas within the study area.

### Reference Data Sources

- **Rivers / Flowlines:** National Hydrography Dataset Plus Version 2.1 — ArcGIS Living Atlas
- **Waterbodies:** National Hydrography Dataset Plus Version 2.1 — ArcGIS Living Atlas
- **Roads:** ArcGIS Living Atlas
- **Municipal Boundaries:** ArcGIS Living Atlas
- **Landmarks:** Manually compiled project features
- **Beach Access:** Manually compiled project features
- **Fishing & Boating Access:** Manually compiled project features
- **Hiking Trails:** ArcGIS Living Atlas
- **Protected Lands:** See **Land Use & Protected Lands** section
- **Watershed Boundary:** See **Watershed Boundary** section

**Processing Notes:**  
Reference layers accessed through ArcGIS Living Atlas were incorporated into the project and prepared as needed for the watershed study area. Locally relevant landmarks and recreational-access locations were manually compiled into project features, including `FishingBoating_Access` and `Beach_Access_Complete`.

Hydrographic, transportation, administrative, recreational, and environmental layers were organized and symbolized within ArcGIS Pro to create the central Watershed Overview map. The completed map was published through ArcGIS Online and incorporated into ArcGIS Experience Builder as the dashboard's primary interactive spatial reference.

The Overview map also displays project-derived protected-land and watershed-boundary information whose original data sources and processing are documented separately in this file.

---

## Land Use & Protected Lands

### National Land Cover Database (NLCD)

**Source:** National Land Cover Database (NLCD), accessed through ArcGIS Living Atlas  
**Data Type:** Land-cover spatial data  
**Geographic Coverage:** United States  
**Purpose:** Identification and analysis of developed land within the Westport River Watershed.

**Project Use:**  
NLCD land-cover data were used to characterize developed areas across the complete watershed study area. Because the source dataset provides national coverage, the same land-cover data could be used across both the Massachusetts and Rhode Island portions of the watershed.

**Processing Notes:**  
Land-cover data were processed to isolate developed land-cover classes and create a watershed-specific developed-area dataset. Intermediate and final outputs included `nlcd_dev_only`, `NLCD_Dev_Polygon`, and `Dev_Areas_Westport`. The resulting developed-area layer was used to calculate watershed-level summary statistics for dashboard visualization.

---

### Protected & Conservation Lands

**Sources:** MassGIS Protected/Open Space data and Rhode Island Conservation Lands data  
**Data Type:** Protected and conservation land polygons  
**Geographic Coverage:** Massachusetts and Rhode Island  
**Purpose:** Identification and analysis of protected land within the Westport River Watershed.

**Project Use:**  
Protected-land data were maintained separately by Massachusetts and Rhode Island and required cross-jurisdictional integration. Massachusetts protected/open-space data were combined with Rhode Island conservation-land data to create a unified protected-lands dataset covering the interstate watershed.

Rhode Island conservation data included permanently protected properties held or protected through ownership, conservation easements, restrictive easements, or deed restrictions by organizations including municipal governments, land trusts, conservation organizations, and federal agencies.

**Processing Notes:**  
Massachusetts and Rhode Island protected-land datasets were prepared and combined into `ProtectedLands_MA_RI_merge`. Additional Rhode Island protected-land polygons were incorporated where needed to complete watershed coverage. The integrated dataset was subsequently processed to create `Protected_Areas_Westport` and used to calculate protected-land summary statistics for dashboard visualization.

---

## Habitat & Biodiversity

### Species Spotlight

**Source:** U.S. Fish and Wildlife Service (USFWS)  
**Data Type:** Species and ecological information  
**Purpose:** Development of the interactive Species Spotlight component of the Westport River Watershed Dashboard.

**Project Use:**  
USFWS species information was used to develop the Species Spotlight section of the dashboard, an interactive biodiversity component designed to introduce users to species associated with the Westport River Watershed and surrounding coastal ecosystem.

**Processing Notes:**  
Species information was researched, organized, and translated into custom digital species cards presenting ecological and identification information in an accessible visual format. The cards were developed using HTML/CSS and integrated into the larger dashboard through ArcGIS Experience Builder.

**Related Project:**  
The Species Spotlight cards and supporting source documentation are maintained in a separate repository:  
[Species Cards — GitHub](https://github.com/AlyssaPacheco2721/species-cards)

---

## Wetlands, Salt Marsh & Sea-Level Rise

### Salt Marsh / Wetlands

**Source:** MassDEP Wetland Polygons Original (1:12,000)  
**Data Type:** Wetland polygons  
**Purpose:** Identification of salt-marsh areas for comparison with a sea-level-rise inundation scenario.

**Project Use:**  
MassDEP wetland polygon data were used to identify and display salt-marsh habitat within the project area. Salt-marsh features were used in combination with sea-level-rise inundation data to create a visual representation of potential coastal exposure.

**Data Note:**  
The source metadata identifies this as a legacy wetlands dataset originally interpreted from 1:12,000-scale aerial photography. MassGIS notes that the dataset has been superseded by an updated statewide wetlands layer and maintains the original dataset for reference purposes.

---

### NOAA Sea Level Rise Viewer Data

**Source:** NOAA Office for Coastal Management — Sea Level Rise Viewer Data Download  
**Source Link:** https://coast.noaa.gov/slrdata/  
**Data Type:** Sea-level-rise inundation spatial data (GeoPackage)  
**Source Files:** `MA_slr_final_dist.gpkg` and `RI_slr_final_dist.gpkg`  
**Scenario Used:** 3-foot sea-level rise  
**Geographic Coverage:** Massachusetts and Rhode Island  
**Purpose:** Visualization of potential sea-level-rise inundation relative to existing salt-marsh habitat.

**Project Use:**  
NOAA Sea Level Rise Viewer data were used to visualize a 3-foot sea-level-rise scenario across the Massachusetts and Rhode Island portions of the project area. The inundation layer was displayed alongside mapped salt-marsh habitat to communicate potential coastal exposure.

**Processing Notes:**  
The NOAA source GeoPackages contained multiple sea-level-rise inundation intervals. The 3-foot scenario was selected for the dashboard and combined with mapped salt-marsh areas to visualize their spatial relationship within the project area.

The resulting map was designed as an environmental communication tool rather than a predictive model of future marsh loss.

---

## Water Quality

### Westport River Water Quality Monitoring Data

**Source:** Westport River Watershed Alliance (WRWA) — River Monitoring Program  
**Source Link:** https://www.westportwatershed.org/river-monitoring  
**Data Type:** Annual water-quality monitoring results and supporting environmental data  
**Geographic Coverage:** Westport River and contributing streams  
**Purpose:** Analysis and visualization of water-quality conditions and multi-year trends within the Westport River.

**Project Use:**  
Published WRWA water-quality monitoring results were used to develop the water-quality component of the dashboard. Monitoring data were compiled across multiple years to examine patterns in coliform bacteria levels across sampling locations and communicate changes in river conditions over time.

The project also incorporated annual rainfall information presented with the monitoring data to provide environmental context for observed water-quality patterns.

**Processing Notes:**  
Published WRWA monitoring results were compiled, cleaned, and reorganized into structured datasets for analysis and visualization. Supporting Excel tables were created from the published monitoring information and prepared for use within the ArcGIS environment. The resulting water-quality data were incorporated into ArcGIS Online and the ArcGIS Experience Builder application.

The dashboard's water-quality component included:

- A multi-year line chart comparing average coliform bacteria levels across seven monitoring locations from 2022–2024
- A 2025 water-quality gauge summarizing mean bacteria conditions using clearly defined water-quality thresholds
- A comparison of annual rainfall conditions from 2022–2024 to provide environmental context for observed water-quality patterns
- Summary annotations interpreting annual rainfall and bacteria exceedance patterns
- Supporting source information derived from WRWA's published monitoring results

The 2022–2024 monitoring visualization was generated from the prepared water-quality dataset within the ArcGIS web environment, allowing differences among monitoring locations and years to be compared directly within the dashboard.

The water-quality component was designed to connect environmental monitoring results with broader environmental conditions and translate technical monitoring data into an accessible public-facing format.

**Data Note:**  
The dashboard represents monitoring data incorporated during the project's development period and is not maintained as a continuously updated monitoring product.

---

## Human Impact & Nutrient Pressure

### Watershed Nutrient Conditions

**Source:** Westport River Watershed Alliance (WRWA) — Watershed Issues  
**Source Link:** https://www.westportwatershed.org/watershed-issues  
**Data Type:** Watershed nutrient conditions, nitrogen targets, and environmental impact information  
**Geographic Coverage:** Westport River Watershed  
**Purpose:** Communication of nutrient pressure and the ecological effects of excess nitrogen within the watershed.

**Project Use:**  
WRWA watershed information was used to develop the Human Impact component of the dashboard. Current and target nitrogen concentrations for the Lower East Branch and Lower West Branch were presented to communicate nutrient pressure within the river and identify conditions exceeding watershed targets.

The dashboard also translated supporting watershed science into an accessible explanation of how excess nutrient inputs can contribute to eutrophication, connecting runoff and nutrient loading with increased algal growth and reduced dissolved oxygen.

**Processing Notes:**  
Published nitrogen concentrations and target values were organized into a comparison table and used to calculate the difference between current and target conditions for each branch.

The Human Impact component included:

- Current and target nitrogen concentrations for the Lower East and Lower West Branches
- Calculated nitrogen overages relative to target conditions
- A simplified visual explanation of the eutrophication pathway
- Sea-level-rise and salt-marsh vulnerability information using the previously documented NOAA and MassDEP datasets
- Examples of watershed-management approaches that can help reduce nutrient inputs and protect natural filtration capacity

The resulting component was designed to connect measured environmental conditions with ecological processes, watershed impacts, and potential management responses in an accessible public-facing format.

---

## Daily Conditions

### Current Weather & Wind Station Data

**Source:** NOAA METAR station data, accessed through ArcGIS Living Atlas  
**Source Service:** https://services9.arcgis.com/RHVPKKiFTONKtxq3/arcgis/rest/services/NOAA_METAR_current_wind_speed_direction_v1/FeatureServer  
**Data Type:** Hourly weather-station observations  
**Update Frequency:** Hourly  
**Purpose:** Display of current environmental conditions within the Daily Conditions component of the dashboard.

**Project Use:**  
The ArcGIS Living Atlas Current Weather and Wind Station Data layer was used to provide automatically updated weather information within the Daily Conditions section of the dashboard. The source layer is generated from hourly NOAA METAR station observations and contains multiple weather variables for monitoring locations.

Station observations were used to display:

- Air temperature
- Wind speed
- Humidity

Only station observations were used for these dashboard indicators; buoy observations available within the source layer were not incorporated.

**Processing Notes:**  
Weather variables were selected from the Living Atlas layer within the ArcGIS Experience Builder environment and configured as individual current-condition indicators. This allowed the Daily Conditions panel to update as new observations became available from the underlying service rather than requiring manual updates to the dashboard.

---

### National Weather Service 72-Hour Precipitation Forecast

**Source:** National Weather Service (NWS), accessed through ArcGIS Living Atlas  
**Source Link:** https://ucdavis-edu.maps.arcgis.com/home/item.html?id=b3ae384875284b8891196a2f132deb81#overview  
**Data Type:** Forecast precipitation spatial data  
**Forecast Period:** 72 hours  
**Purpose:** Visualization of regional forecast precipitation conditions.

**Project Use:**  
The National Weather Service 72-Hour Precipitation Forecast layer was incorporated into the Daily Conditions section as an interactive map providing regional precipitation context.

Rainfall information was included because precipitation and runoff are important environmental context for interpreting water-quality conditions within the watershed.

**Processing Notes:**  
The Living Atlas precipitation forecast layer was embedded within the ArcGIS Experience Builder application and displayed as a regional forecast map rather than a project-derived analytical product.

---

### NOAA Tide Predictions

**Source:** NOAA Tides & Currents  
**Source Link:** https://tidesandcurrents.noaa.gov/noaatidepredictions.html?id=8447791&legacy=1  
**Station:** NOAA Station 8447791  
**Data Type:** Tide predictions  
**Purpose:** Access to current and upcoming tidal conditions relevant to the Westport River coastal environment.

**Project Use:**  
The Daily Conditions component included a direct connection to NOAA tide predictions, allowing dashboard users to access tidal information alongside current weather and precipitation conditions.

**Processing Notes:**  
Rather than reproducing or manually maintaining tide predictions within the dashboard, users were directed to the NOAA tide-prediction resource for the selected station.

---

### Live Data Integration

The Daily Conditions component was designed to complement the dashboard's historical and project-period environmental analyses with automatically updating environmental information. Current weather observations and forecast precipitation were incorporated through ArcGIS Living Atlas services, while tidal information was connected directly to NOAA's tide-prediction resource.

This approach allowed the dashboard to combine historical monitoring, spatial analysis, environmental interpretation, and current environmental conditions within a single public-facing application.
