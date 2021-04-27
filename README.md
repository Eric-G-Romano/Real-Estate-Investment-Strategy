![](images/Hudson_county_.PNG)
# Real Estate Investment Statergy 
### Author: Eric Romano
## Overview
One of the many questions that are asked about investments is why should you invest in real estate vs the stock market. As 
of 2018, the total equity capitaliztion in the US stock market was $30.4 trillion, while US real estate was estimated to 
be worth $49.3 trillion. There are two main reasons why Americans will continue to favor real estate as a long term investment
1. More consistency 
2. Less volatilty 

## Business Problem 
A Real-Estate Investment Firm from North Jersey picked up on a growing demand from residents in NYC and their ever-growing
desire to leave and head to New Jersey. The Investment firm reached out to my Consultant company to provide them direction
into specific areas in Hudson County. The proximity to NYC is hard to beat and a transportation system already established
makes this county the perfect location to explore. We are task to explore this area and determine the best zip codes in
Hudson County to invest in. 
1.	Can we successfully use the available data to predict future ROI’s for all the zip codes in Hudson County? 
2.	What zip codes present the best ROI’s to in 2018 and 2019? 
3.	What investment strategies can be formulated by using the available data set provided by Zillow?
4.	Can we build a tool that streamline prediction models and limit complexity to reduce time and cost? 

### Hyptheses
Null Hypothesis (H0): The historical data does not persist over time and cannot be used to make predictions

Alternative Hypothesis (Ha) The historical data does persist over time and can be used to make predictions 

## Data Understanding 

Zillow provides their users the opportunity to use their platform to access specific datasets for research purposes. 
The dataset that we will be using contains the median home sales prices throughout all states sorted by their zip codes. 
With this dataset you can extract a lot of insight through out all states with the potential to understand markets and 
develop investment strategies. This platform allows the public to do independent research in any market in the US. 

This dataset contains 14723 rows and 272 columns 

## Method

The analysis performed in my main Jupiter notebook follows a CRISP-DM method approach. Using a reputable dataset, I was 
able to use the data to make predictions of future home values price. To achieve this the first step is to transform the 
data format into a long format that is required when performing time series analysis. Understanding the best problem was 
key in this analysis as we narrowed down our search to select all the zipcodes in Hudson County. Using time series 
analysis and modeling techniques I was able to develop an investment strategy that focused in selecting the top zipcodes 
in Hudson County to possibly invest in. Using SARIMAX models I was able to create various models that used different 
lag orders allowing us to use past data that persist onto the future. However, to avoid complicated and computationally 
costly models I selected using AutoARIMA function to streamline the process and cut down on the complexity of the models.

<img src="https://github.com/Eric-G-Romano/dsc-phase-4-project/blob/main/images/Stationarity_check.png" width="500" height="500"> 

To achieve stationarity with all the time series, representing the median home sale prices, I performed differencing twice.

## Results 

![](images/ROI%20for%20Zipcodes%20in%20Hudson%20County.png.PNG) 

For our final model we determined that the best location to begin investing in is found in the graph above. All but one zipcode 
in Jersey City presents the best possible ROI for the year of 2018. Looking at our risk to reward profile we see that highest 
coefficient of variations (CV) falls right below 2.5. Comparatively, the ETF has a higher CV of 2.6. This suggests that these 
markets provide a safer investment relative to that of investing in other securities.

<img src="https://github.com/Eric-G-Romano/dsc-phase-4-project/blob/main/images/ROI%20for%20Zipcodes%20in%20Hudson%20County.png" width="500" height="500">

## Evaluations

## Conclusion

In conclusion, The Zillow median home sale prices are a great dataset to develop insights that will help in the processes
of formulating an investing strategy. With this dataset you can transform this data into a time series to run analysis 
to see if certain historical patterns persist over time. However, the model does not perform well under situations that 
can not be foreseen. With this mind our ARIMA models should be used to make predication at most 1 year out as the result 
become unreliable as you continue to increase the time frame. You can also streamline this process with other markets 
besides Hudson county as it seems like the simple model performs well with mostly all the zip codes.

### Recommendations 

1. Continue to invest heavily in Jersey City as the market still has room for potential returns
2. I would also begin to make strategic steps to enter areas like Weehawken, North Bergen, Union City and West New York.
Eventually when Jersey City becomes over saturated, like Hoboken, these other towns provide promising returns
3. Consider entering the development space as the need for parking spaces is a problem for all these areas. By building
studio apartment with parking spaces your firm would surely capitalize on the growing demand to head to North Jersey

### Future Work 

Due to the inability for the model to correctly adjust to unique events the best way to prepare for this is to understand
the relationship between these home sale values with exogenous data. The ones that I wish to explore are interest rates,
national debt, unemployment rates, rent values, and GDP. This will allow us to develop a better exist strategy if we 
understand how each market reacts to each exogenous variable. 
I also would like to create interactive dash boards for those that are interested on using these models and would like 
to explore other areas in the US. 
Lastly, I would like to see if these same models will be effective with more recent years and how recent events affects
and impact the usefulness of these models.  

## For More Information

Please review my full analysis in my [Jupyter Notebook]() or my [presentation]().
For any questions, please contact Eric Romano at egustavo94@gmail.com 

For any additional questions, please contact **Eric Romano** at [egustavo94@gmail.com](egustavo94@gmail.com).

## Repository Structure

```bash

├── README.md                                   < The top-level README for reviewers of this project
├── Mortgage_Loan_Denial_Classification.ipynb   < Narrative documentation of analysis in Jupyter notebook
├── Mortgage_Loan_Denial_Classification_ppt.pdf     < PDF version of project presentation
├── Mortgage_Loan_Denial_Classification.pdf     < PDF version of Jupyter notebook
├── data                                        < CSV file used for this project
├── image                                       < Visualizations generated for analysis
└── images                                      < Visualizations generated for analysis
```
