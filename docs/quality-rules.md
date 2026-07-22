# Declared Data-Quality Rules

The experiment evaluated seven controlled defect categories:

| Category | Injected records |
|---|---:|
| Duplicates | 500 |
| Missing salaries | 300 |
| Invalid ages | 200 |
| Negative balances | 150 |
| Malformed customer IDs | 100 |
| Invalid geography values after normalization | 50 |
| Invalid gender values after normalization | 50 |

The validation workflow reported:

- 850 rule-invalid records;
- 500 duplicate records;
- 1,350 quarantined records;
- 9,150 Silver records; and
- 9,150 Gold records.

The Gold validation reported zero duplicate customer IDs and zero null
engineered features.

The eventual code release should map each rule to a named function,
expected input type, failure reason, and test case.
