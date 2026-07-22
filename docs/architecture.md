# Architecture

## Five-layer framework

1. **Trusted ingestion**  
   Access to Azure Data Lake Storage Gen2 is established through an
   Azure Databricks Access Connector using managed identity. Azure RBAC
   authorizes storage access without embedded account keys or secrets.

2. **Bronze layer**  
   Source records are ingested into Delta tables with minimal
   transformation, preserving the experimental input for traceability.

3. **Quality validation and quarantine**  
   Deterministic rules identify invalid values and malformed identifiers.
   Duplicate records are isolated separately. Invalid and duplicate
   records are written to Quarantine rather than silently discarded.

4. **Silver layer**  
   Valid, unique records are standardized and persisted as governed
   Delta tables.

5. **Gold layer**  
   Engineered features and analytics-ready records are produced from
   Silver data and validated for uniqueness and feature completeness.

## Implemented controls

- managed identity;
- Azure RBAC;
- Unity Catalog;
- storage credentials and external locations;
- Delta Lake tables;
- deterministic validation;
- duplicate detection; and
- quarantine routing.

## Out-of-scope controls

The evaluated prototype does not claim implementation of:

- attribute-based access control;
- dynamic data masking;
- row-level filters;
- production-scale adversarial testing; or
- multi-user behavioral evaluation.

These remain future extensions.
