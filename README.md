# Data-Portfolio

## About

I am currently a Postdoc in Mathematics in a subfield called 'Geometric Anlaysis' - https://arxiv.org/search/math?searchtype=author&query=Wondo,+H. In my spare time I enjoy learning and doing data analysis. This repository is a collection projects I have done. 

## Data Projects

### Maven Coffee Sales
**Code:** [`Analysis_of_Coffee_Sales`](https://github.com/hwondo/Data-Analysis-Portfolio-Files/blob/main/Maven_coffee_sales.ipynb)

**Goal:** Understand Sales Trends Across (Fictional) Coffee Shops in New York

**Data:** https://www.kaggle.com/datasets/agungpambudi/trends-product-coffee-shop-sales-revenue-dataset?resource=download

**Summary:** This analysis is largely exploratory in nature. We use pandasql to query and manipulate the dataset to produce plots for sales trends across different time scales - hourly, daily and yearly. Averages are taken over the data set for each time scale to obtain the trends of a 'typical' day and week.  

We show a distinctive trend in sales over the year and average total hourly sales. Furthermore, we show strong correlation between similar product types. 


### Geospatial and Sentimental Analysis for Seattle Airbnb Dataset

**Code:** [`Analysis_Sattle_Airbnb`](https://github.com/hwondo/Data-Analysis-Portfolio-Files/blob/main/Seattle_Airbnb_analysis.ipynb)

**Goal:** Create a regression model that gives recomendations for reservation price. 

**Data:** https://www.kaggle.com/datasets/swsw1717/seatle-airbnb-open-data-sql-project

**Summary:** The analysis shows a difference in revenue generated throughout the year across different neighborhoods. Each trend follows a weekly cycle with peaks corresponding to weekends. The best performing neighborhood group is the miscellaneous group called 'other neighborhood', followed by 'Downtown' throughout the first three months of the 2024 financial year.

Furthermore, we establish spatial autocorrelation in the data using Ridley's K function, the Getis'Ord'G statistical test and a hjeat map using Kernel density estimation. We encode this spatial data into regression models in the following way:
- Model 1: no geometric data. This will be used as a base model to compare our performance.
- Model 2: includes neighborhood group as a categorical variable.
- Model 3: includes neighborhood as a categorical variable
- Model 4: includes cluster groups obtained previously as a categorical variable
- Model 5: includes longitude and latitude as lagged terms in a geometric regression.

In our final regression model, we apply an OLS regression with neighborhood as a categorical variable and sentiment as a continuous variable. Sentiment is calculated from the reviews of each listing. Tested on a validation set, the model produces predictions with an MSE of 0.04517.

### Evaluation of Regression Techniques on Housing Price Data

**Code:** [`Analysis_Housing_Regression`](https://github.com/hwondo/Data-Analysis-Portfolio-Files/blob/main/Housing%20Prices%20Prediction%20Models.ipynb)

**Goal:** Evaluate various regression models using a comprehemsive evalaution method by Zhan-Liu-Wu-Zhao-Chow (https://www.sciencedirect.com/science/article/abs/pii/S0957417423014835#sec4).

**Data:** https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data

**Summary:** In this project, we build a variety of industry standard regression models and rank them using a method in "A hybrid machine learning framework for forecasting house price" by Zhan-Liu-Wu-Zhao-Chow (https://www.sciencedirect.com/science/article/abs/pii/S0957417423014835#sec4). The standard insutry regression methods we use are:
- Ordinary Least Squares Lasso regression
- Random Forest Regression
- Ada Boosted regression
- Nearest neighbors regression
- Support vector machine.

The evalution method uses 13 evaluation metrics and ranks each model for each metric. The models are then ranked by their mean ranking for each metric. A Friedman and Iman–Davenpor test is used to test for significant variation in the rankings for each model across the evaluation metrics. 

**Results:** Using the evaluation procedure described above, we obtain a 'best' performance model, which in our case is an OLS Lasso model. However, the statistical tests reveal that there is no significant difference in performance of the five standard models used.



