---
title: NYC Yellow Taxi Data Project using Fabric
date: 2025-12-20
category: Data Engineering
excerpt: a complete end-to-end data engineering and analytics solution implemented using Microsoft Fabric for NYC Yellow Taxi trip data (January– October 2025)
collection: portfolio
---
## Project Overview

This implementation reflects production-style data engineering practices. The objectives were to:  

* Ingest monthly Parquet files into a Fabric Lakehouse
* Load raw data into a Warehouse staging layer
* Cleanse and validate incoming records
* Enrich trip data with taxi zone lookup data
* Transform and model data in a presentation layer
* Maintain full historical data (append model)
* Log per-run metadata for automation and auditability
* Automate the month-over-month processing workflow
* Expose data via a Fabric semantic model for Power BI reporting

The project was completed using Microsoft Fabric’s Data Factory, Lakehouse, Warehouse, Dataflows Gen2, SQL stored procedures, and Power BI.

## Data Sources

### 1. NYC TLC Yellow Taxi Trip Data (Parquet)

Ten monthly Parquet files (January–October 2025), each containing 3–4 million rows.

![](/images/portfolio/NYC-Yellow-Taxi-Data-Project/nyctaxi_yellow_uploaded_files.png)

### 2. Taxi Zone Lookup (CSV)

Maps `LocationID` to borough, zone, and service zone.  

![](/images/portfolio/NYC-Yellow-Taxi-Data-Project/lookup_zones_csv_uploaded.png)

