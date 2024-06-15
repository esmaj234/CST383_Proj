# Introduction
&nbsp; With the rising cost of housing, it can be difficult for families and individuals to afford to own a home. With house prices and inflation seemingly increasing every year, budgeting to purchase a home seems like a daunting task.
<br>
<br>
&nbsp; There is a general rule in finance that one’s housing costs should account for no more than 33% of their household income. We are looking to estimate if one can stay within the 33% allotment given a dataset on home price and income information. We will train our model on this dataset to see what way home prices versus household income are trending in the coming years to find the affordability of owning a home in the United States.
<br>
<br>
# Selection of Data
https://www.kaggle.com/datasets/joshhaber/us-real-estate-incomepriceregion-census-data
<br>
<br>
&nbsp; We are starting with this dataset from Kaggle, which depicts the prices people paid for homes between 2014 - 2022, as well as their relationship to average income. The dataset also provides income information, adjusts for inflation, and accounts for geographical region, average sale price, number of households, median income, and mean income.
<br>
<br>
&nbsp; As with any dataset, we will need to run analysis and perform data cleaning that way, we have a reliable source to train our learning model on. Ideally, this would have been a larger sample size but we are confident that this dataset is a great starting point to train our model as it is objective and we can easily add additional data and run the inflation conversion to generate more information.
<br>
<br>
# Methods
&nbsp; To answer our research question we used a linear regression machine learning model. To train it we used five different predictors to find the average home sales price. 
<br>
<br>
&nbsp; We were initially interested in finding affordability as our target; but we realized that affordability calculations relied on both the average home price and median income so we could not use those columns from the dataframe. Doing this, the model was essentially a flat line because the other columns were the year, region, and home size, so no financial data. We did,  however, create columns that assigned each region and each home size with a unique integer so that we could incorporate them into our model.
<br>
<br>
&nbsp; We ended up reworking the project by designating the target as the average home price and used the median income as a predictor. From there, we found the affordability and plotted it over time using one example with the income as the current 2024 median income. We elected to use the median income versus the mean income because it represents the exact center of income distribution which reduces the impact of income levels that can skew the data.
<br>
<br>
&nbsp; In the end, we used a line graph to plot the initial affordability of a home, which was around 10% of a person’s income going to housing costs. Because the affordability function was directly correlated to both the predictor of median income and the target of the average home price, we have a smooth linear graph.
<br>
<br>
# Results
&nbsp; To determine what percentage of a person’s income went to their household expenses, we created a function that accounts for the initial down payment, loan interest rate, property tax, and homeowners insurance to get an accurate result.
<br>
<br>
&nbsp; Looking at the final graph, we can see when a home’s affordability will pass the suggested threshold. Our example, where a person is looking for a single-family home in the midwest and their income is the current median income will hit this threshold by 2040. 
<br>
<br>
# Discussion
&nbsp; Our findings found that there exists a relationship between home prices and income as time goes on. As expected, prices vary greatly across different regions and property sizes. However, it was interesting to see how income levels also influence the home prices. We’ve also learned that the predictors we chose are significant in providing reasonable conclusions and insight based on the dataset. 
<br>
<br>
&nbsp; Our findings are also consistent with current research trends. Home prices are rising steadily, in part due to limited housing supply and an increase in demand. Our results on affordability are in step with the growing disparity between income growth rate and housing costs. Future research would greatly benefit from larger datasets with additional factors such as regional rates, particularly in terms of property tax and homeowner’s insurance, two key elements of actual affordability.
<br>
<br>
&nbsp; That being said, we do wish there was a larger sample size of data so we could better train our model. For example, the home prices on the coast of California are grouped into the same region as less expensive homes in other west coast states. Having this insight could further scope our research into certain areas. It also would have been nice to have the full list of incomes, instead of only the median. That way we could see how affordability looks over a broader range of incomes.
<br>
<br>
# Summary
&nbsp; Our project ultimately highlights the complex relationship between income and home prices and their effect on affordability in the housing market. Understanding trends in the housing market leads to proper financial planning. Based on our current model, it appears that 33% of a person’s income is sufficient to afford purchasing a home. However, our model also shows that by approximately 2040, that will no longer be the case, and the required portion of a person’s income needed to support their housing costs only rises.
<br>
<br>
So to answer our original question:
<p style="text-align: center;"><em>Home Sweet Loan: Can You Afford Your Dream Home?</em></p>
<p style="text-align: center;"><em>As home prices freely roam, prepare to earn more to make it your own...</em></p>

<br>
# Bibliography
Down Payment Estimation: https://www.forbes.com/advisor/mortgages/average-down-payment-on-a-house/

Property Tax Figures:
https://www.bankrate.com/real-estate/property-tax-rates-us/#:~:text=The%20effective%20average%20property%20tax,to%201.16%20percent%20in%202018.

Homeowners Insurance Premiums:
https://www.iii.org/fact-statistic/facts-statistics-homeowners-and-renters-insurance

Average Median Income - US - 2022
https://datacommons.org/place/country/USA?utm_medium=explore&mprop=income&popt=Person&cpv=age,Years15Onwards&hl=en

