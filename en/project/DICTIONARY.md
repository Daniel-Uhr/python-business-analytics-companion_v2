# Data dictionary — Swan Supermarkets



The fictional chain has five stores in one city and a Swan+ loyalty program. Synthetic data serve education and describe no real company. The customer file is a synthetic random sample of 3,000 customers registered before 2025, observed January–December 2025. One row is one customer.



| Column | Meaning and unit |

|---|---|

| customer_id | Text ID M0001–M3000; identifiers are preserved across editions |

| store | Registration reference store: Downtown, North, South, East, West |

| age | Age in years in 2025 |

| household_income | Declared monthly household income, USD thousands per month; blank if unreported |

| distance_km | Straight-line distance from registered address to reference store, km |

| signup_channel | Program signup: store, app, or website |

| uses_app | Used the app at least once during 2025: 1 yes, 0 no |

| coupon | Assigned monthly coupons for 2025: 1 yes, 0 no |

| visits | Number of purchases registered in the program during 2025 |

| annual_spend | Total purchases registered in 2025, USD |

| renewed | Renewed membership for 2026: 1 yes, 0 no |



## Business rules



In December 2024, each eligible customer independently had probability 1/2 of coupon assignment, without requiring equal group sizes. The annual cost was approximately USD 120 per assigned customer, including discounts and delivery. Average gross margin is 20% of sales. For the instructional calculation, cost is incremental and not already deducted from the margin. Real accounting must confirm whether sales and margins already include discounts; never count them twice.



App use is a customer choice, not randomized. Purchases without card identification are not recorded; zero registered visits is possible. Any individual, including small-business owners buying for resale, may join. Income is self-reported, unverified, and optional. Renewal is not observed future revenue. No staffing, hours, or wage variables are present.



## Optional monthly revenue file



One row is one month, January 2016–December 2025. `month` is YYYY-MM; `revenue_thousands` is total chain monthly revenue in USD thousands, seasonally adjusted by the planning team. It is not the total of the customer sample.



## Localization and integrity



Column/category labels are translated; numbers, missing entries, IDs, and order are unchanged. USD at the same magnitudes localizes a fictional case; no exchange-rate conversion occurred. Preserve CSV files and transform in the notebook. Hash agreement verifies bytes, not substantive data quality.



`customers_swan.csv`



SHA-256: `55ab66e43714208b571c7c451e028051dfb23343c23747083125c4a3bb51a231`



`monthly_revenue_swan.csv`



SHA-256: `19fabb9bde915d21a1efddaa46730594c82c59924f76e928e5c035751e0fdf23`

