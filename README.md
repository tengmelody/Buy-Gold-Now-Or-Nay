Buy Gold Now Or Nay

Predicting Gold Prices with Sentiment Analysis of Public Opinion

The economic market has been particularly volatile this year. The pandemic, paired with US political disarray, has casted uncertainties among speculators.

The erraticism made gold a particular appealing commodity. After all, the conventional wisdom has always been to buy the metal during times of crisis.

Troubled times produce fears of economic collapse and currency depreciation. In turn, speculators turn to gold.

Unlike the fiat money system, gold's value comes from its inherent worth. Money's value is relative. Gold is gold.

Before money came into existence, gold was the main form of currency. Gold thus holds a special historical, cultural significance.

This project is to examine whether market/social crisis provokes gold prices to go up.

If there is an ongoing economic apprehension (due to Covid, US election, etc.), should we then invest in gold?

Using data from Reddit's 'worldnews', I compiled daily comments since the onset of Covid. The purpose here is to discern if the general world outlook is negative. This was done by conducting a sentiment analysis on the words and comments. Do they lean positive or negative?
NLTK's Vader sentiment analysis indicated that since Covid, the world outlook has been pretty.... neutral.

As expected, the world's sentiment level fluctuated up and down on a daily level. At the end of the day, all the yo-yoing trickled down to just white nosies that dwells over a constant mean level.

![Image](https://github.com/tengmelody/Capstone2_Buy_Gold_Now_Or_Nay/blob/master/img/Are%20we%20all%20going%20to%20hell%3F.png)

Next was the gold prices analysis.

The data came from World Gold Council and comprised of daily gold prices from the past year. I delimited the data criteria to range from beginning of Covid and in US dollars.

The gold data is an additive time series since its seasonality is constant over time.

I wanted to see how gold was trending. Was there panic-induced buying of gold? If so, was there an upward trend of gold prices?

I performed seasonal decomposition analysis to isolate the trend component from the data. Removing seasonality and residuals allowed for clearer reading of trend.

![Image](https://github.com/tengmelody/Capstone2_Buy_Gold_Now_Or_Nay/blob/master/img/gold%20seasonal%20decompose.png)

Gold trend showed a remarkable increase, especially since February. That month also marked the start of Covid news coverage and spread of infections.

Furthermore, gold reached a record high of $2000 per ounce at around that month... For the first time in history.

So my "hunch" in gold really manifested from this notable piece of information on gold.

But the rationale was to see whether the surge could be explained by economic/ social stress. And if we could apply the same logic in future situations to make similar predictions.

So, positive gold rates paired with neutral social sentiments? Is there a correlation?

Doing a Pearson's Correlation (numpy's corrcoef) indicated a result close to zero. -0.04, to be more precise.

![Image](https://github.com/tengmelody/Capstone2_Buy_Gold_Now_Or_Nay/blob/master/img/corr.png)

My data analysis showed a lack of clear relationship between the two elements.

I wanted to see if gold would be a good investment for the near future, but data seemed to say nay.

But what if the world got worse? Some catastrophic event befell humanity? That would make world sentiment and outlook much more dire, wouldn't it? In that case, a stronger negative correlation could be squeezed out then. So let's wait a few more years and revisit this topic again then.
