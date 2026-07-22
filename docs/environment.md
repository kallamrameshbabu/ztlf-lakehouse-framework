# Execution Environment

This repository contains a sanitized implementation of the Zero-Trust Lakehouse Framework (ZTLF) experimental workflow.

## Required platform

The notebooks are designed for an Azure Databricks environment with:

- Apache Spark
- Delta Lake
- Unity Catalog
- Azure Data Lake Storage Gen2
- An Azure Databricks Access Connector or another approved managed-identity configuration

No workspace URL, tenant identifier, subscription identifier, storage account name, access token, secret, or connection string is included in this repository.

## Runtime version

The exact Databricks Runtime version used in the original experiment is not recorded in the publication package. Before claiming exact reproduction, record and publish the runtime version used for the rerun.

A current Databricks Runtime that supports the Spark and Delta Lake APIs used by the notebooks should be selected and documented by the reproducing user.

## Required permissions

The executing identity requires permission to:

1. Read the source CSV from the configured ADLS Gen2 path.
2. Create and use the configured Unity Catalog catalog and schema.
3. Create, replace, read, and write the Bronze, Silver, Gold, and quarantine Delta tables.
4. Use any external location, storage credential, or managed-identity resource configured by the workspace administrator.

Follow the principle of least privilege. Do not place credentials directly in notebook cells.

## Configuration

Copy:

```text
config/example_config.json
```

to a local or workspace-specific configuration file and replace the placeholder values. Do not commit the filled configuration file when it contains private infrastructure names.

## Execution order

Run the notebooks in this order:

1. `notebooks/00_platform_foundation.ipynb`
2. `notebooks/01_bronze_ingestion.ipynb`
3. `notebooks/02_create_experimental_dataset.ipynb`
4. `notebooks/03_data_quality_validation.ipynb`
5. `notebooks/04_gold_ai_ready.ipynb`

## Reproducibility boundary

The repository provides the implementation and experimental workflow. Independent end-to-end reproduction also requires:

- a compatible source dataset obtained lawfully by the reproducing user;
- a configured Azure Databricks workspace;
- ADLS Gen2 access;
- Unity Catalog permissions; and
- environment-specific configuration.
