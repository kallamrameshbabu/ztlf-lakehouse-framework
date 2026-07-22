# Databricks notebooks

These notebooks implement the experimental workflow described in the associated ZTLF manuscript.

## Execution order

1. `00_platform_foundation.ipynb`
2. `01_bronze_ingestion.ipynb`
3. `02_create_experimental_dataset.ipynb`
4. `03_data_quality_validation.ipynb`
5. `04_gold_ai_ready.ipynb`

## Prerequisites

- Azure Databricks workspace with Unity Catalog enabled
- Permission to create schemas, volumes, and Delta tables
- Azure Data Lake Storage Gen2 source location
- Secretless storage access, preferably through an Azure Databricks Access Connector and managed identity
- A licensed or synthetic CSV matching the schema used by `01_bronze_ingestion.ipynb`

## Public-release safeguards

All notebook outputs have been removed. The public source path uses placeholders, and no credentials, access keys, tokens, tenant IDs, subscription IDs, workspace URLs, or personal email addresses are included.

The catalog name `dbx_niw_analytics` and schema name `ztlf` are examples and may be replaced for another environment.

## Reproducibility limitation

The original `Churn_Modelling.csv` acquisition record and redistribution license were not preserved. Do not upload that dataset unless its authoritative source and license are confirmed. A synthetic dataset with the same schema is recommended for public execution.
