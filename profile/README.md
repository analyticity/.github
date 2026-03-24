# Analyticity

**Analyticity** is a data-driven application for analyzing, integrating, and simulating urban traffic data.  
It combines heterogeneous data sources, advanced data modeling, and simulation capabilities to support decision-making in urban mobility and traffic management.

---

## Overview

Analyticity is designed as both:
- a **research platform** for developing and validating data integration and traffic analysis methods, and  
- a **production-oriented application** for real-world usage and experimentation.

The system integrates multiple traffic-related datasets (e.g., accidents, jams, closures, alerts) into a unified model, enabling:
- analysis of historical and real-time traffic data  
- simulation of traffic scenarios  
- visualization of urban mobility patterns  

---

## Architecture

The platform follows a modular architecture:

### 1. Data Sources
- Official data from ŘSD (Ředitelství silnic a dálnic ČR) 
- Crowd-sourced traffic data (e.g., Waze: jams, closures, alerts)  
- Official police accident records  

### 2. Data Integration
- Matching and merging heterogeneous datasets  
- Spatial-temporal alignment of events  
- Data cleaning, validation, and enrichment  

### 3. Unified Data Model
Core entities:
- Accidents  
- Jams  
- Closures  
- Alerts  
- Providers and event links  

All data is standardized into a consistent schema to enable cross-source analysis.

### 4. Data Storage
- Time-series and relational database (e.g., TimescaleDB / PostgreSQL)  
- Supports:
  - recent (near real-time) data  
  - aggregated historical data  

### 5. Application Layer
- Multi-instance application (different cities and scenarios)  
- Provides:
  - data exploration  
  - analytics  
  - visualization  

### 6. Simulation Engine
- Simulation of:
  - accidents  
  - closures and their impact  
  - traffic scenarios  

---

## Key Features

- Integration of heterogeneous traffic data sources into a unified system  
- Advanced spatial-temporal matching of events across multiple providers  
- Unified data model enabling consistent analysis across datasets  
- Support for both real-time and historical traffic data processing  
- Modular architecture allowing separation of data ingestion, processing, and application layers  
- Simulation capabilities for evaluating the impact of traffic events (e.g., closures, accidents)  
- Multi-city support with configurable data pipelines  
- Reproducible data processing and experiment workflows  
- Designed to bridge research and real-world application deployment  

---

## Repository Structure

| Repository | Description | **Open to public**
|-----------|------------| -----------|
| `demo-application` | Main application (FE+BE) - only demo version on sample data | Public | 
| `routing-server` | BE application for finding route between 2+ points in Brno | Public | 
| `waze-data-analysis` | FE application, currently running on github pages, TO-BE-DELETED | Public | 
| `PoliceAndWazeSpatioTemporalMatching` | Jupyter notebook focusing on matching police data to waze data in Brno | Private |  


> The main entry point of the project is the **`demo-application`** repository.

---

## Application Demo

A running demo of the application is available at:  
https://analyticity.github.io/waze-data-analysis/

**Note:**
- The current demo represents an **earlier version** of the application  
- It does **not use the internal Analyticity database**, but instead connects to the **City of Brno public API**  
- Only the **Brno (Czech Republic)** use case is supported in this version  

---

## Research Context

This project is developed as part of a **PhD research** focused on:
- integration of heterogeneous traffic data sources  
- spatial-temporal data matching  
- urban traffic modeling and simulation  

The platform serves as both:
- an experimental environment  
- and a validation tool for proposed methods  

---

## Citation

This project has resulted in (and continues to support) scientific publications in the area of traffic data analysis and integration.

Ondrušková, M., Hynek, J., & Burget, R. (2025).  **[Towards Street-Level Traffic Analysis Using Waze Crowdsourced Data.](https://ieeexplore.ieee.org/abstract/document/11037686/)** *2025 Smart City Symposium Prague (SCSP)*. IEEE. 

--- 

## Contact

Magdaléna Ondrušková  
Brno University of Technology, Faculty of Information Technology  
Email: iondruskova@fit.vutbr.cz  

---
## Contributing

This project is developed with the support of students contributing as part of their **Bachelor's and Master's theses**.

Contributors (by year, alphabetically):
- 2025, Bc. Matyáš Strelec – Routing Algorithm for Traffic Planning in Brno [thesis](https://www.vut.cz/studenti/zav-prace/detail/164964)
- 2025, Bc. Veronika Šimková – Analysis and Visualization of Traffic Accident Data [thesis](https://www.vut.cz/studenti/zav-prace/detail/164963)

---
## Acknowledgements

This work was carried out under the supervision of:

- Ing. Jiří Hynek, Ph.D.  
- doc. Radek Burget, Ph.D.  

I would like to sincerely thank them for their guidance, patience, and continuous support throughout my PhD studies. Their insights, feedback, and willingness to discuss ideas have been invaluable not only for this project, but for my research as a whole.

---

## Note

This project is under active development as part of ongoing research.
