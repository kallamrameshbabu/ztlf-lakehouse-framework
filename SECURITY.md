# Security Policy

## Reporting

Do not disclose credentials or exploitable cloud configuration in a
public issue. Contact the repository owner privately through the email
listed on the author's ORCID record.

## Sensitive material

Never commit:

- Azure tenant or subscription identifiers when avoidable;
- storage account keys or SAS tokens;
- service-principal secrets;
- Databricks personal access tokens;
- workspace or cluster credentials;
- private endpoints or internal hostnames;
- real customer data; or
- employer-confidential code and documents.

The repository demonstrates architectural patterns and deterministic
data-quality behavior. It is not a production security baseline.
