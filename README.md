## SC1015-INTRO-TO-DATA-SCI-ART-INTELL
Introduction to Data Science and Artificial Intelligence  
Mini Project - Resale Flat Prices

## Problem Definition
The data science problem that we have created is to:
1. Identify the drivers for each generations (1990s, 2000s, 2010s and 2020s).
2. Observe if recession affects the resale prices for specific flat types and models
* Flat Type - 3, 4, 5 room and executive 
* Flat Model - improved, new generation, model a, standard, simplified, maisonette and apartment
3. Better analyse the factors which contributes to the increase of resale prices.
 
So as to better perform financial planning when purchasing a resale flat.

## Data Cleaning
We have engaged a professional property agent to better understand the dataset that we are handling and have performed date cleaning for the following columns: 
* Individual Town to Region
* Combined Storey Range
* Sorted Years into Decades
* Calculation of Lease
* Cleaning of Flat Type and Flat Models
 
A text file(data_description.txt) has been created for detailed descriptions for each of the columns.

## Exploratory Data Analysis
1. Looking at the resale price line graph from 1990 to 2022 based on flat types. We inferred that there are some flat types, which (apartment) prices only rise back to its previous peak vs (the rest) prices that have reached an all time high. We have mentioned the increase and decrease of resale prices based on certain factors such as recession, economy recovery and supply-and-demand.
2. Flat Type vs Region - We observed that most of the 3 room resale flats are located in the Central region and most of the 4 room resale flats are located in the West region. However, when we compare the data as a whole, we have actually calculated and found that most of the resale flats are located in West region.
3. Resale Price vs Region - We observed that despite the fact that most resale flats are located in West region in previous slide, the resale price peaks for East region in 1990s and 2000s, while the peak has shifted to Central region in 2010s. Thus, we can conclude that number of resale flats in sale for a certain region does not significantly affect resale prices of that region. When we compare the data as a whole, we will realise that resale price actually peaks for North-East region instead of the previous regions mentioned.
4. Map Visualisation of the resale price peaks had been preparerd as mentioned previously for better illustration. Peak for East region in 1990s and 2000s, peak for Central region in 2010s. Overall, peak for North-East region.
5. Resale Price vs Flat Model - We observed that the resale prices has increased over the past decades in general. And that those rare flat models (i.e. Type S) are of high value in current market.
6. Correlation Matrix - We observed that the correlation between floor area sqm and resale price has fallen over the decades. Correlation between floor area sqm and lease left briefly increased but drops down. Correlation between resale price and lease left briefly increased but not significant enough to be noted. As a whole, we concluded that while the correlation between floor area sqm and resale price has fallen over the decades, they are still linearly correlated to a certain extend. For the rest, they are not correlated so much to resale price, especially lease left (which is almost close to 0).

## Machine Learning Models
1. Linear Regression
2. Random Forest Regression

## Linear Regression  
1. Model Evaluations: 
We observed that lease_left have become an important variable to determine resale price. That is because holding all other features fixed, a 1 unit increase in lease_left is associated with an increase of $1400 in period of 2010 to 2019. Compared to previous decades where it has a value of -$3700 and -$800.
2. Model Predictions:  
For the period of 1990 to 1999, the model have a positive correlation of 0.40 against the test data. 
The residuals distribution is skewed to the right.
For the period of 2000 to 2009, the model have a positive correlation of 0.57 against the test data. 
The residuals distribution is also skewed to the right.
For the period of 2010 to 2019, the model have a positive correlation of 0.67 against the test data. Which is the highest across all three decades. 
The residuals distribution is slightly skewed to the right. 
3. Model Comparisons:  
R2: We can see that the lowest explained variance (R-Squared), MSE and RMSE value is in the 2010s period.

## Random Forest 
1. From the training datasets, OOB Rsquared score estimate and cross validation score gets closer with each gen. The 2010s data is seen to have the best scores, fitting the model the best.

2. From observations, the biggest nonnumerical driver is flat type. Out of all the non-numerical variables other than flat types, flat model_model A affects the price in 1990s the most, while region_Central affects the price in 2000s and 2010s most. 

3. Out of all the generations, 2010's would be the most similar to 2020s as seen from the score being the best. As such, we can predict that the drivers for 2020s would likely be similar to 2010s drivers. 
 
## Conclusion and Takeaways
Drivers affecting each period: Flat models and region plays a big part in the increase of resale prices. 
* 1990s and 2000s: Most of resale prices peak for the East region.
* 2010s: Most peak for Central region.  
 
We have also previously mentioned that despite the fact that floor area sqm are going down as decades pass, the resale price still continues to increase.

* Recession: We have also went through the fact that recession actually affects the resale prices, making that period a good time to purchase resale flats.

* Linear Regression: We have learnt that using linear regression model against time series data, works best with data that are much closer to the current date.

* Random Forest Regression: Similar to Linear Regression model, the random forest regression models tend to have better score with data that are much closer to the current date.

Both algorithms show that 2010s data is more similar to the 2020s, hence we can use that generation's data to aid our financial planning when purchasing resale flats.

## Contributors
@joxywfs - JOEY LIM HUI MING  
* Interviewed Property Agent
* Data Cleaning
* Exploratory Data Analysis  
* Slides and Script
 
@Sa3manthaLim - LIM SHI TONG  
* Data Cleaning
* Exploratory Data Analysis  
* Random Forest Regression
* Slides
 
@jastjs - TOH JING SHENG  
* Data Extraction & Cleaning
* Exploratory Data Analysis
* Linear Regression
* Slides

## References
* Resale Flat Prices https://data.gov.sg/dataset/resale-flat-prices
* Singapore Regions https://data.gov.sg/dataset/master-plan-2019-subzone-boundary-no-sea
* Map Visualization https://plotly.com/python/mapbox-county-choropleth/
* Correlation and Linear Regression http://sites.utexas.edu/sos/guided/inferential/numeric/bivariate/cor/
* Residual Plot Histogram https://www.originlab.com/doc/Origin-Help/Residual-Plot-Analysis
* Linear Regression https://www.udemy.com/course/python-for-data-science-and-machine-learning-bootcamp/
