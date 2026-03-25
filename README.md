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

<img width="1823" height="907" alt="image" src="https://github.com/user-attachments/assets/b743f3bc-a583-43b1-82c1-26f5b48a48ac" />
<img width="1791" height="423" alt="image" src="https://github.com/user-attachments/assets/a7d1e8d2-6cca-4477-b01b-729067d9e702" />
<img width="1375" height="748" alt="image" src="https://github.com/user-attachments/assets/bafd3ddc-ce13-4132-9be6-840315056ca2" />
<img width="1409" height="378" alt="image" src="https://github.com/user-attachments/assets/bb590477-6bb6-43c6-b823-ab1c2fad42fe" />









## Author
Lennix Stevens
