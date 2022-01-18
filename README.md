# investment

The most recent project is "two_types.ipynb" and "only_prices.ipynb".
The first one needs tickers to input. In the latest version (Jan 2022), it downloads the ticker list from SBp exchange, works with the file, and finally deletes it from your PC.
Then after running all the cells we get 2 tables "boost.xlsx" and "growth.xlsx", both includes about 100+ companies.
The first one is about small-cap fast growing companies with relatively high risk.
The second one is about large growing companies with relatively low risk.
All the companies inside are sorted by so called "Score" value. The more - the better. The score is calculated in a special manner, that can be seen in the code.
Shortly, we take all the basic financial parameters, then tail very large positive and negative values, then normalize values from 0 to 1 and take the sum as a Score.

![image](https://user-images.githubusercontent.com/67582707/149946710-71041772-0c65-4f6c-8395-dd7b09cb3ab8.png)

Afterwards, we need to deside, whether the stock is cheap or not. There are plenty of aproaches, but I take the mix of the following:

1. Current P/E relative to median historic P/E.
2. Current P/S relative to median historic P/S.
3. Price levels (are calculated here as largest price clusters).
4. RSI (14).
5. Some ML magic as dependencies between margins/growth and current P/S (should take more historical data for proper work).

The investing decision still remains with every investor.
