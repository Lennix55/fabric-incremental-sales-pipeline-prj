# Incremental Sales Pipeline (Microsoft Fabric)

## Overview
This project simulates a production-grade incremental data pipeline using Microsoft Fabric and Lakehouse architecture.

The pipeline ingests headerless tab-delimited sales files (2019–2021), processes only new data using file tracking and watermark logic, and builds analytics-ready Gold tables.

---

## Architecture

Medallion Architecture:

Raw Files → Bronze → Silver → Gold

- Bronze: Raw ingestion with enforced schema
- Silver: Cleaned and deduplicated transactional data
- Gold: Aggregated business reporting tables

---

## Technologies Used

- Microsoft Fabric
- Spark (PySpark)
- Lakehouse
- Delta Tables
- Data Pipelines
- SQL MERGE (UPSERT)
- Incremental Processing

---

## Key Features

✅ Incremental ingestion using processed file tracking  
✅ Schema enforcement for headerless files  
✅ Idempotent pipeline execution  
✅ MERGE-based upsert logic  
✅ Automated pipeline scheduling  
✅ Medallion architecture implementation  

---

## Incremental Strategy

1. Raw files land in `/Files/raw`
2. Pipeline checks `processed_files` table
3. Only unseen files are ingested
4. Data cleaned in Silver layer
5. Gold tables updated using MERGE

---

## Results

The pipeline processes new sales data without reprocessing historical files, simulating real enterprise data engineering workflows.

---

## Author
Lennix Stevens
