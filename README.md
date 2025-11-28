# Spatial-Modelling
Application of spatial regression models (Spatial Lag and Spatial Error) to investigate the determinants of Tuberculosis incidence in Kenya using R. Includes code for data simulation, Moran's I calculation, and cluster mapping.
# Spatial Analysis of Tuberculosis Incidence in Kenya 🇰🇪

This repository contains a spatial econometric analysis of Tuberculosis (TB) incidence across 47 counties in Kenya. The project was conducted as part of the **STA 3010: Statistical Modeling** coursework.

## 📌 Project Overview
The goal of this analysis was to identify geographical clusters of TB and determine the socio-economic drivers of the disease while accounting for spatial dependence.

## ⚙️ Methodology
The analysis follows a structured spatial modeling workflow using **R**:
1.  **Data Preparation:** Integration of simulated disease data with Kenya's administrative shapefiles.
2.  **ESDA (Exploratory Spatial Data Analysis):**
    * Choropleth mapping of incidence rates.
    * Global Moran's I to test for spatial autocorrelation.
    * LISA (Local Indicators of Spatial Association) to identify "Hotspots" (High-High clusters).
3.  **Spatial Regression Modeling:**
    * Comparison of OLS (Ordinary Least Squares), SLM (Spatial Lag Model), and SEM (Spatial Error Model).
    * Model selection based on AIC and residual diagnostics.

## 🔍 Key Findings
* **Clustering:** Strong positive spatial autocorrelation was observed (Moran's I = 0.286), with significant hotspots identified in the Northern arid regions.
* **Modeling:** The **Spatial Error Model (SEM)** provided the best fit (lowest AIC), indicating that unobserved regional factors (clustering of errors) explain the variance better than direct contagion.
* **Drivers:** Population density was identified as a significant positive driver of TB incidence after controlling for spatial effects.

## 🛠️ Tech Stack & Libraries
* **Language:** R
* **Spatial Data:** `sf`, `geodata`
* **Visualization:** `tmap`
* **Modeling:** `spdep`, `spatialreg`

