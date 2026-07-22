# Reproducibility Status

## Available

This repository provides:

- sanitized Databricks notebooks;
- the notebook execution order;
- an environment and permissions guide;
- a configuration template;
- expected experimental record counts; and
- the documented Bronze, validation, quarantine, Silver, and Gold workflow.

## Not included

This repository does not include:

- Azure credentials or secrets;
- private workspace or storage identifiers;
- deployed Azure infrastructure;
- the original source CSV;
- a guarantee of exact runtime equivalence; or
- production-scale benchmark evidence beyond the experiment described in the manuscript.

## Status statement

> Implementation and experimental workflow available; independent end-to-end reproduction requires users to obtain a compatible source dataset separately and configure an appropriate Azure Databricks environment.

## Scope limitation

The repository should not be interpreted as experimental validation of features not evaluated in the manuscript, including row-level security, attribute-based access control, dynamic data masking, production-scale performance, or machine-learning model quality.
