# Security and Sanitization Notes

The public notebooks have been prepared to avoid disclosure of environment-specific or confidential values.

## Values that must not be committed

Do not commit:

- access tokens;
- account keys;
- client secrets;
- connection strings;
- SAS tokens;
- passwords;
- tenant or subscription identifiers;
- private workspace URLs;
- private storage account or container names;
- client or employer names;
- confidential catalog, schema, table, or external-location names; or
- personal email addresses and local paths.

## Safe configuration practice

Use workspace configuration, approved secret management, managed identity, and least-privilege access. Keep public configuration files limited to placeholders and non-sensitive defaults.

Before every public release, search the repository for:

```text
token
secret
password
account_key
client_secret
connection_string
sas
tenant
subscription
https://adb-
abfss://
@*.dfs.core.windows.net
```

A search match is not automatically a secret, but every match should be reviewed.
