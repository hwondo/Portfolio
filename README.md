## About

I am currently a Postdoc in Mathematics conducting research in 'Geometric Analysis' - https://arxiv.org/search/math?searchtype=author&query=Wondo,+H, H. In my spare time, I enjoy learning about math-related fields such as data analysis and cryptography. This repository is a collection of projects I have done. 

My CV: 

## Table of contents
- [About](#about)
- [Data Projects](#data-projects)
    + [Predicting Stock Buybacks](#buyback)
    + [Geospatial and Sentimental Analysis for Seattle Airbnb Dataset](#geospatial-and-sentimental-analysis-for-seattle-airbnb-dataset)
- [Cryptography Projects](#cryptography-projects)
    + [RSA and ElGamal](#rsa-and-elgamal)
    + [Elliptic Curve](#elliptic-curve)

## Data Projects

### Predicting Stock Buybacks

**Code:** [`Predicting Stock Buybacks`]((https://github.com/hwondo/Stock_Buybacks))

**Goal:**  Create a machine learning pipeline for predicting stock repurchases that
- Gathers data obtained from multiple sources (SEC Edgar, St. Louise FRED and finance).
- Trains and tunes machine learning models to predict stock buybacks.
  
**Data:** Data is obtained from the following sources:
- Stock data from Yahoo Finance and indices.
- Financials from 10-Q and 10-K SEC filings reports.
- Download economic data from FRED.

**Summary:** 
We create two models that predict stock repurchases (buybacks). The model takes inputs consisting of company, stock market and economic data for each quarter and predicts buyback status for the next quarter. More precisely, the first model performs a classification task, predicting whether a buyback will occur. The second model performs a regression task and predicts the cash (in USD) a company will spend on buybacks in that quarter. 

Our final model is a Random Forest Classifier with a weighted F1 score of 0.74 when tested on an unseen validation set. Our final regression model is a single-layer Feedforward Neural Network model with an RMSE score of 1.1373 when tested on an unseen validation set.

### Geospatial and Sentimental Analysis for Seattle Airbnb Dataset

**Code:** [`Analysis_Sattle_Airbnb`](https://github.com/hwondo/Portfolio-Files/blob/main/Seattle_Airbnb_analysis.ipynb)

**Goal:** Analysis for Airbnb listings: 
- Spatial data visualisation and analysis using Folium maps, Ripley K and Getis-Ord statistics. 
- Produced a time series forecast for revenue using seasonal decomposition. 
- Created a regression model for price recommendations, involving spatial weights and sentiment from reviews. 

**Data:** https://www.kaggle.com/datasets/swsw1717/seatle-airbnb-open-data-sql-project

**Summary:** The analysis shows a difference in revenue generated throughout the year across different neighbourhoods. Each trend follows a weekly cycle with peaks corresponding to weekends. The best performing neighbourhood group is the miscellaneous group called 'other neighbourhood', followed by 'Downtown' throughout the first three months of the 2024 financial year.

Furthermore, we establish spatial autocorrelation in the data using Ridley's K function, the Getis'Ord'G statistical test and a heat map using Kernel density estimation. We encode this spatial data into regression models in the following way:
- Baseline Model: no geometric data. This will be used as a base model to compare performances.
- Model 1: includes neighbourhood group as a categorical variable.
- Model 2: includes neighbourhood as a categorical variable
- Model 3: includes cluster groups obtained previously as a categorical variable
- Model 4: includes longitude and latitude as lagged terms in a geometric regression.

In our final regression model, we apply an OLS regression with neighbourhood as a categorical variable and sentiment as a continuous variable. Sentiment is calculated from the reviews of each listing. Tested on an unseen validation set, the model produces predictions with an MSE of 0.1008.


## Cryptography Projects 

### RSA and ElGamal 

Python code that implements RSA and ElGamal.

**Code:** [`RSA and ElGamal`](https://github.com/hwondo/cryptography/blob/main/RSA_DiffieHellman.ipynb)

### Elliptic Curve

Python code that implements elliptic curve key exchange and the ElGamal algorithm.

**Code:** [`Elliptic Curve Cryptography`](https://github.com/hwondo/cryptography/blob/main/Elliptic_Curve.ipynb)


