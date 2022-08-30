# DS-Project-9-Forecasting_Store_Sales_TimeSeriesAnalysis
Designed a model that Forecasts Store Sales.

* Forecasts are very important for bussinesses and stores as they must be aware of how much inventory to buy. Predict a little over, and stores are stuck with overstocked, perishable goods. Guess a little under, and popular items quickly sell out, leading to lost revenue and upset customers.Thanks to Data Science and Machine Learning, we can get more accurate forecasts.
* Dataset - Part of a Kaggle competition. Dataset contains grocery store data sales from Corporación Favorita, a large Ecuadorian-based grocery retailer.
* Model - The major aim in this project is to build a model that more accurately predicts the unit sales for thousands of items sold at different Favorita stores using Time Series Analysis methods and Deep Learning algorithms.

## Code and Resources Used ##
**Python Version:** 3.10.5 <br />
**Packages:** pandas, numpy, keras, matplotlib, seaborn, statsmodels, warnings  <br />
**For Web Framework Requirements:** _pip install -r requirements.txt_ <br />
**Data Resources:** <https://www.kaggle.com/competitions/store-sales-time-series-forecasting/data>

## About the Dataset ##

The training data includes dates, store and product information, whether that item was being promoted, as well as the sales numbers. <br>

Additional files include supplementary information very important for time series analysis are provided. They are as follows: <br>
- stores.csv - Store metadata, including city, state, type, and cluster 
- oil.csv - Daily oil price. Includes values during both the train and test data timeframes.Ecuador is an oil-dependent country and it's economical health is highly      vulnerable to shocks in oil prices. <br>
- holidays_events.csv - Holidays and Events, with metadata.Important factor that affects store sales largely. <br>
[Note:  Also has additional information for more complex analysis] 



## EDA - Exploratory data analysis ## 
- Dropped null values .
-
## Model Building ##
I also split the data into train and tests sets with a test size of 20%.

I tried three different models and evaluated them using Mean Absolute Error. I chose MAE because it is relatively easy to interpret and outliers aren’t particularly bad in for this type of model.

I tried three different models:

Multiple Linear Regression – Baseline for the model
DecisionTree Regression – Because of the sparse data from the many categorical variables, I thought a normalized regression like DecisionTree would be effective.
Random Forest – Again, with the sparsity associated with the data, I thought that this would be a good fit.

## Model Performance ##
The Random Forest Regression model outperformed the other approaches on the test and validation sets.I found out the Mean and the Standard Deviation for all the three models. This basically gives us an image by how much percentage can the predictions be off the actual prediction.
* **Multiple Linear Regression:**   Mean- 5.028337074958086 , Standard Deviation- 1.056869119278954
* **Decision Tree Regression:** Mean- 4.256820741921791,
   Standard Deviation- 1.1575140416039331
* **Random Forest Regression:** Mean- 3.304827981052571, 
   Standard Deviation- 0.6490112395533792 <br />
The results were pretty good since in the worst case scenario,our predictions would only be off by a meager 3.65%.
