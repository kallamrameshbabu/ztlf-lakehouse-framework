# Reproducibility Plan

## Current status

The manuscript reports a completed Azure Databricks implementation.
This public repository currently contains documentation and release
scaffolding, not a verified executable reproduction package.

## Required information before code release

Record the following directly from the implementation environment:

- Azure region;
- Databricks Runtime version;
- Spark version;
- Delta Lake version;
- Unity Catalog configuration;
- cluster or SQL warehouse configuration;
- Python and library versions;
- storage container layout;
- catalog, schema, and table naming conventions;
- notebook execution order;
- random seed or deterministic defect-injection procedure;
- validation-rule definitions; and
- expected record counts and assertions.

## Proposed execution order

1. Provision or identify the governed Azure environment.
2. Configure managed-identity access.
3. Create storage credentials and external locations.
4. Ingest the licensed or synthetic source into Bronze.
5. Generate the controlled experimental defects.
6. Apply validation and duplicate detection.
7. Route rejected records to Quarantine.
8. Publish valid unique records to Silver.
9. Engineer Gold features.
10. execute record-count, uniqueness, and null assertions.

## Release criterion

Do not label the repository reproducible until a clean environment can
execute the documented workflow and reproduce the declared counts.
