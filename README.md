# GIS-Project2-EE-DuckDB
# Project 2: Integrating Google Earth Engine Raster Data with DuckDB Vector Layers

## Overview

This project demonstrates an integrated geospatial data science workflow that combines cloud-based raster analysis from Google Earth Engine with locally stored vector data managed in DuckDB. The objective is to explore how environmental variables such as precipitation and temperature relate to real-world geographic features such as parks and waterways.

The analysis focuses on the Kalamazoo, Michigan area and uses interactive mapping and spatial analysis techniques to investigate environmental patterns.

---

## Objectives

- Utilize at least two raster datasets from Google Earth Engine  
- Integrate at least two vector datasets stored in a database (DuckDB)  
- Perform spatial analysis linking raster and vector data  
- Demonstrate exploratory geospatial analysis and workflow development  

---

## Data Sources

### Google Earth Engine (Raster Data)
- GRIDMET Dataset  
  - Precipitation (`pr`)  
  - Maximum Temperature (`tmmx`)  

### Vector Data (OpenStreetMap via OSMnx)
- Parks (leisure features)  
- Waterways (hydrological features)  

---

## Methods

### 1. Earth Engine Processing
- Accessed GRIDMET dataset
- Filtered by:
  - Spatial extent (Kalamazoo area)
  - Temporal range (Summer 2024)
- Generated:
  - Total precipitation raster
  - Mean maximum temperature raster

### 2. Vector Data Acquisition
- Retrieved OpenStreetMap features using OSMnx
- Converted to GeoDataFrames
- Cleaned and clipped to study area

### 3. Database Integration (DuckDB)
- Created a DuckDB database (`project2.duckdb`)
- Stored vector attributes as tables:
  - `parks`
  - `waterways`
- Performed SQL queries to explore data

### 4. Spatial Analysis
- Converted vector data to Earth Engine FeatureCollections
- Applied zonal statistics:
  - Extracted raster values over parks and waterways
- Calculated summary metrics:
  - Park area
  - Waterway length

### 5. Visualization
- Used geemap to create interactive maps
- Displayed:
  - Precipitation (blue gradient)
  - Temperature (warm color ramp)
  - Parks and waterways layers

---

## Key Results

- Successfully integrated raster and vector datasets within a single workflow  
- Demonstrated how climate variables can be associated with landscape features  
- Showed spatial relationships between precipitation, temperature, and environmental features  

Due to the coarse spatial resolution of the GRIDMET dataset, results represent generalized climate patterns rather than fine-scale variations.

---

## Tools and Technologies

- Python  
- Google Earth Engine  
- geemap  
- DuckDB  
- GeoPandas  
- OSMnx  

---

## Project Structure
