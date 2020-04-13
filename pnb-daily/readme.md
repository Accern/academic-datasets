# Public News & Blogs Sample with Daily Aggregation

Accern data is collected through news or social media websites and computes
numerical metrics like sentiment, relevance, republication (i.e., impact), etc.
on the text data. One row in the CSV contains the date, ticker (i.e., name of
the stock), multiple target values (price change), as well as, Accern features
aggregated using functions such as mean, min, max, etc. in hourly windows.

The data is aggregated for price prediction on market open. That is, aggregates
are computed in hourly segments up until the 8.00am-9.00am EST time window of
the date of the prediction. (as the market opens at 9.30am EST, it would be
possible to utilize predictions for executing orders).
The data set does not contain any accidental or intentional
leak of information from the future at any point (except in the target columns).
As there are multiple target columns, make sure to _remove_ the other target
columns in order to avoid label leakage.

## pnb1h.csv.zip:

| column | description |
| :---   | :---   |
| date | The date of the row. |
| ticker | The ticker symbol of the stock. |
| :---   | :---   |
| | Make sure to remove the other target columns to avoid label leaks. |
| open | The price at market open. |
| next_open | The price at market open of the following day. |
| oo | The price change between today's open and the following open. |
| oo | The binary price change between today's open and the following open. |
| :---   | :---   |
| | All columns are prefixed with the number of hours before market open. 1h_count is the event count for the time span 8.00am-9.00am, 2h_count the time span 7.00am-8.00am, etc. |
| xh_count | The number of events collected by Accern in the current time slice. |
| xh_&ast;_sum | The sum of the values of the given feature &ast; in the current time slice. |
| xh_&ast;_min | The minimum value of the given feature &ast; in the current time slice. |
| xh_&ast;_max | The maximum value of the given feature &ast; in the current time slice. |
| xh_&ast;_avg | The average value of the given feature &ast; in the current time slice. |