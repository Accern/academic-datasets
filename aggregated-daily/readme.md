# Sample with Daily Aggregation

Accern data is collected through news or social media websites and computes
numerical metrics like sentiment, relevance, republication (i.e., impact), etc.
on the text data. One row in the CSV contains the date, ticker (i.e., name of
the stock), pricing data of the previous date, volatility data (using the
volatility index [VIX](https://en.wikipedia.org/wiki/VIX))
of the previous date, the target (relative change of the
price from today to tomorrow), as well as, Accern features aggregated using
functions such as mean, min, max, etc.

The data is aggregated for price prediction on market open. That is, aggregates
begin 9.30am EST of the previous day until 9.30am EST of the current day
(so it would be possible to utilize predictions for executing orders just after
the market opens). The data set does not contain any accidental or intentional
leak of information from the future at any point (except in the target column).
For the most basic classification prediction task the target column needs only
to be converted into binary form such that values larger than zero mean
"stock price going up over the next day" and the opposite for other values.

| column | description |
| :---   | :---   |
| date | The date of the row. |
| ticker | The ticker symbol of the stock. |
| target | The target value (price change from today's open price to next day's open price). |
| prev_day_open | The open price on the previous market day. |
| prev_day_close | The close price on the privous market day. |
| prev_day_high | The highest price on the privous market day. |
| prev_day_low | The lowest price on the privous market day. |
| prev_day_vix_open | The open price of VIX on the previous market day. |
| prev_day_vix_close | The close price of VIX on the privous market day. |
| prev_day_vix_high | The highest price of VIX on the privous market day. |
| prev_day_vix_low | The lowest price of VIX on the privous market day. |
| count | The number of events collected by Accern from yesterday 9:30am until today 9:30am. |
| &ast;_sum | The sum of the values of the given feature &ast; from yesterday 9:30am until today 9:30am. |
| &ast;_min | The minimum value of the given feature &ast; from yesterday 9:30am until today 9:30am. |
| &ast;_max | The maximum value of the given feature &ast; from yesterday 9:30am until today 9:30am. |
| &ast;_avg | The average value of the given feature &ast; from yesterday 9:30am until today 9:30am. |
