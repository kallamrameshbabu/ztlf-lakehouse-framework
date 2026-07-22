# Notebooks

Add sanitized Databricks source notebooks only after verifying that they
contain no confidential identifiers, credentials, proprietary code, or
employer-owned material.

Recommended sequence:

1. `01_ingestion`
2. `02_controlled_defect_injection`
3. `03_quality_validation`
4. `04_quarantine_and_silver`
5. `05_gold_feature_engineering`
6. `06_experimental_assertions`

Each notebook should document inputs, outputs, dependencies, and expected
record counts.
