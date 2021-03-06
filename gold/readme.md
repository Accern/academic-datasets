# Sample of Gold Price

Predicting gold price using complementary data streams.

*The target column needs to be shifted by at least one row to not leak the label*

| column | description |
| :---   | :---   |
| date | The date |
| nominal_effective_exchange_rate | Nominal Effective Exchange Rate |
| effective_federal_funds_rate | Effective Federal Funds Rate |
| cpi_index | Consumer Price Index |
| djia_adj_close | Dow Jones Adjusted Close |
| gold_price | The current gold price (value of previous target) |
| :---   | :---   |
| target | Regression Target |

The file `gold_price_target.csv` excludes the `gold_price` column but is
otherwise the same.

Disclaimer: This data is for research purposes only, provided 'as is',
and solely for informational purposes, not for trading purposes or advice.
