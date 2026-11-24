# RAND Health Insurance Experiment data notes

The bundled randhie.csv contains 20,190 person-years from the historical US RAND Health Insurance Experiment. Families were assigned to insurance plans with different coinsurance rates, the percentage of covered expenses paid by the participant. The chapter uses 14,941 person-years from plans without an individual deductible, with rates of 0%, 25%, 50% and 95%.

| Field | Definition |
|---|---|
| mdvis | Number of outpatient physician visits during the year. The binary outcome equals one when this count exceeds zero. |
| lncoins | Natural log of one plus coinsurance in percent. Recover the rate with round(exp(lncoins) − 1). |
| idp | Indicator for an individual deductible plan. Select zero for the chapter sample. |
| lpi | Log of the annual participation incentive, floored at one before taking logs. |
| fmde | Zero for individual deductible plans. Otherwise the log of the maximum of one and the maximum dollar expenditure divided by the coinsurance fraction. |
| physlm | Physical limitation indicator. |
| disea | Number of chronic diseases. |
| hlthg, hlthf, hlthp | Self-rated health indicators for good, fair and poor. Excellent is the reference. |

**Provenance.** The project source record identifies the CSV as a byte-for-byte snapshot from statsmodels 0.14.5, dated November 4, 2026. SHA-256 is 7ee0d2dea0ca8ecfcfbb02c31d63a88abe632318f5a110d638d6a035f4827f91. The notebooks load this local file. The statsmodels documentation describes the dataset as public domain and notes small differences from the subset reported by Cameron and Trivedi (2005). [Dataset documentation](https://www.statsmodels.org/stable/datasets/generated/randhie.html)

**Interpretation.** The RAND study assigned families to plans. Individuals contributed repeated years and some participants left the experiment. The extract lacks person and family identifiers, so the chapter cannot calculate family-clustered standard errors. The annual indicator measures whether an outpatient physician visit occurred. Hospital stays, spending and health benefits are separate outcomes. Comparisons with current insurance settings require attention to changes in prices, access and care delivery.
