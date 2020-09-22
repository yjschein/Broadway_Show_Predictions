
# Predicting the Price of Hamilton Tickets


## Project Overview
The goal of this project was to predict the price of Hamilton tickets. I web scraped the data and gathered the weekly gross of every broadway show from 1985. I shortened this data set to only include the show Hamilton and changed the gross column (my target variable) to monthly gross. To clarify, this column is not the sum of all the weekly gross in a month, it is the average of all the weekly grosses for each month.

## Purpose / Business Understanding
Predicting the gross of broadway tickets is important for a few reasons. First of all, if a show is not reaching its full potential then it is very likely that the show will fail. Stakeholders that will be intersted in this problem are people that want to invest in broadway shows and make a profit. The broadway industry makes billions of dollars every year and each broadway show costs millions of dollars to produce. And the number one way that a show makes money is by selling tickets. If someone can predict the weekly/monthly gross of a broadway show then they will be able to know which shows they should invest in. 

## Data Preperation
The code was very clean and did not contain any missing values, however, I did change a few things. I downsampled the data set so its monthly instead of weekly. Additionally, after building some baseline and regular models, I added some exogenous variables to see if that had an effect on the RMSE. More details to the changes that I made to the data are in the notebook. 

![/Documents/Flatiron/Flatiron_FinalProject/df_year.png](https://github.com/yjschein/Flatiron_FinalProject)

![Year](/Documents/Flatiron/Flatiron_FinalProject/df_year.png)
![Month](/Documents/Flatiron/Flatiron_FinalProject/df_month.png)
![Week](/Documents/Flatiron/Flatiron_FinalProject/df_week.png)

## Modeling
The best baseline model was an ARIMA model which gave me an RMSE score of around 160000. This means that the average weekly gross of a month in 2019 was off by an average of $160,000. This is not bad considering that the average weekly price of a month in 2019 is around $3,000,000. I also included ARIMA, ARIMAX, SARIMA, and SARIMAX in the data set. The best model was a SARIMA model with an RMSE of $130,000. 

