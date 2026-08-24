# Westport River Watershed Dashboard

**Environmental GIS Analysis & Interactive Data Visualization**

An interactive GIS project integrating spatial, ecological, water-quality, land-use, climate, and environmental data to explore conditions across the **Westport River Watershed in Massachusetts and Rhode Island**.

The project combines environmental data from multiple agencies and jurisdictions into a unified watershed-scale framework. GIS processing, environmental data analysis, cartographic visualization, and web GIS development were used to examine watershed characteristics and communicate environmental conditions through an interactive dashboard.

---

## Project Overview

The Westport River Watershed Dashboard was developed as a self-directed environmental GIS project focused on bringing multiple dimensions of watershed health into one accessible platform.

The project required working with environmental datasets maintained separately across Massachusetts and Rhode Island, including data from **MassGIS, RIGIS, NOAA, USGS, EPA/MassDEP, and other environmental data providers**.

Major components include:

- Watershed boundary development and cross-jurisdictional data integration
- Land-use and protected-land analysis
- Multi-year water-quality analysis and visualization
- Habitat and biodiversity mapping
- Sea-level-rise and coastal habitat vulnerability visualization
- Human-impact indicators
- Live environmental conditions
- Interactive species information
- Web GIS development and environmental communication

---

## Technical Workflow

### 1. Watershed Boundary & Data Integration

Environmental data for the watershed were distributed across separate Massachusetts and Rhode Island datasets.

A unified study boundary was created by integrating appropriate **MassGIS and RIGIS watershed data**, allowing subsequent analyses to represent the complete study area rather than only the Massachusetts portion.

Working across jurisdictions required identifying comparable datasets, cleaning and preparing spatial data, managing coordinate systems, and integrating layers into a common GIS environment.

### 2. Land-Use Analysis

Land-use analysis incorporated Massachusetts and Rhode Island spatial datasets to characterize development and protected land within the watershed.

The workflow included:

- Preparing and cleaning land-use and conservation datasets
- Integrating Massachusetts and Rhode Island spatial data
- Clipping environmental data to the watershed study area
- Processing developed-land and protected/open-space layers
- Calculating watershed-level summary statistics
- Visualizing the proportion of developed and protected land

Results were incorporated into the dashboard through thematic mapping, summary statistics, and data visualization.

### 3. Water-Quality Analysis

Multi-year water-quality monitoring data were cleaned, organized, summarized, and visualized to communicate changes in watershed conditions.

Outputs included:

- Multi-year water-quality trend visualization
- Summary and callout statistics
- Water-quality indicator graphics
- Interactive dashboard components designed to provide context for environmental measurements

### 4. Habitat & Biodiversity

Spatial habitat datasets were integrated to visualize ecologically important areas and biodiversity within the watershed.

The biodiversity component was expanded through custom interactive species cards developed with HTML/CSS and embedded within ArcGIS Experience Builder.

### 5. Sea-Level Rise & Coastal Vulnerability

NOAA sea-level-rise information was incorporated with wetland and habitat data to visualize potential coastal exposure.

A **3-foot sea-level-rise inundation scenario** was used to explore the spatial relationship between projected inundation and salt-marsh habitat within the study area.

This component was designed as a visualization of potential exposure rather than a prediction of future habitat loss.

### 6. Interactive Web GIS Development

Processed GIS layers and environmental information were published through ArcGIS Online and assembled into an interactive watershed application.

Interactive elements included:

- Thematic environmental maps
- Land-use statistics
- Water-quality trends and indicators
- Habitat and biodiversity information
- Sea-level-rise visualization
- Environmental callout statistics
- Custom species information
- A live **Daily Conditions** panel incorporating current environmental and NOAA information

---

## GIS & Data Processing

The project involved a range of GIS and environmental data-management techniques, including:

- Multi-source environmental data acquisition
- Data cleaning and organization
- Attribute and tabular joins
- Cross-jurisdictional spatial data integration
- Coordinate-system management and reprojection where required
- Spatial clipping and polygon processing
- Summary-statistic calculations
- Land-use and conservation analysis
- Thematic and unique-value symbology
- Existing ArcGIS layer (`.lyr`) integration
- Cartographic design
- ArcGIS Online publishing
- Interactive web GIS development

---

## Tools & Technologies

- **ArcGIS Pro** — spatial data preparation, analysis, geoprocessing, and cartography
- **ArcGIS Online** — web GIS hosting and publishing
- **ArcGIS Experience Builder** — interactive application development
- **QGIS** — supporting GIS data preparation and visualization
- **Microsoft Excel** — environmental data cleaning, organization, and analysis
- **HTML/CSS** — custom interactive species-card components

---

## Data Sources

The project integrates environmental and geospatial information from multiple authoritative sources, including:

- Massachusetts Bureau of Geographic Information (**MassGIS**)
- Rhode Island Geographic Information System (**RIGIS**)
- National Oceanic and Atmospheric Administration (**NOAA**)
- U.S. Geological Survey (**USGS**)
- U.S. Environmental Protection Agency (**EPA**)
- Massachusetts Department of Environmental Protection (**MassDEP**)
- Habitat and biodiversity data from state and federal environmental programs
- Local watershed and water-quality monitoring information

Detailed dataset documentation will be maintained in [`docs/data-sources.md`](docs/data-sources.md).

---

## Related Project: Watershed Species Cards

The dashboard's biodiversity component includes a collection of interactive species cards developed to provide accessible ecological information about organisms associated with the Westport River Watershed.

The cards were developed separately using HTML/CSS and incorporated into the larger dashboard through ArcGIS Experience Builder.

➡️ **[View the Species Cards Repository](https://github.com/AlyssaPacheco2721/species-cards)**

---

## Project Documentation

Additional technical documentation is available in:

- [`Methodology`](docs/methodology.md) — detailed GIS and analytical workflow
- [`Data Sources`](docs/data-sources.md) — environmental datasets, agencies, and source documentation

---

## Project Presentation

A visual overview of the project and dashboard components is available here:

➡️ **[View the Westport River Watershed Dashboard Project](https://alyssapacheco.webflow.io/work/westport-dashboard)**

---

## Skills Demonstrated

`Environmental GIS` `Spatial Analysis` `Watershed Science` `Environmental Data Analysis` `Water Quality` `Land-Use Analysis` `Coastal GIS` `Climate Vulnerability` `ArcGIS Pro` `ArcGIS Online` `Experience Builder` `QGIS` `Data Visualization` `HTML/CSS`

---

## Author

**Alyssa Pacheco**  
Environmental Scientist | GIS & Coastal Science
