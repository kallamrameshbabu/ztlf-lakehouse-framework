# Expected Experimental Results

The following values are the principal integrity checks reported for the controlled experiment.

| Checkpoint | Expected record count |
|---|---:|
| Original source records | 10,000 |
| Experimental records after controlled additions | 10,500 |
| Rule-invalid records | 850 |
| Records valid before deduplication | 9,650 |
| Injected duplicate records | 500 |
| Final Silver/Gold records | 9,150 |

## Validation equations

The counts should satisfy:

```text
10,500 - 850 = 9,650
9,650 - 500 = 9,150
```

## Interpretation

- The 850 rule-invalid records should be routed to the quarantine path or table.
- The 9,650 records that pass rule validation are evaluated for duplicates.
- Removing the 500 injected duplicates produces 9,150 final records.
- The final Gold output should contain the same record population as the deduplicated Silver output unless the Gold notebook intentionally applies an additional documented filter.

## Important qualification

These values are expected for the controlled experiment described in the manuscript. A different source dataset, different random seed, altered validation rules, or modified defect-injection logic can produce different results.

Before publishing a reproduction claim, retain the Databricks job output, table-history information, and relevant aggregate counts.
