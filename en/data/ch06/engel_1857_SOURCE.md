# Engel household food expenditure data

The file `engel_1857.csv` contains 235 records for working households in Belgium in 1857. Each row represents one household. Both `income` and `foodexp` are annual amounts in Belgian francs. Keep the original precision when calculating a share, covariance or slope.

The local file is a byte-for-byte snapshot of the Engel CSV distributed with statsmodels 0.14.5. Its SHA-256 digest is `05b60e091325bc170cb6803ce78f80c029bfe2ae072891ec577f1ebe8deefd61`. The source documentation describes the dataset as public domain. Koenker and Bassett (1982), *Robust Tests for Heteroscedasticity Based on Regression Quantiles*, is the associated empirical reference. [Dataset documentation](https://www.statsmodels.org/stable/datasets/generated/engel.html)

These historical observations contain no household size, regional prices or location controls. Their association cannot identify an individual household’s causal response to a change in income.
