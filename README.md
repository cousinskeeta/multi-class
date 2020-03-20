# Multi-classification Model with Stock Data

## Introduction
This model required web scraping and API skills, building pipelines and tuning hyperparameters for supervised classification algorithms. This repository includes the `Multi-classification Model notebook`, the final stock dataset (`Stock_Dataset_13`), as well as the scrapping notebooks sub-repo used to scrape and combine all the stock data used here, `Stock_Data_Web_Scrappers`.  

##  Question: <i>What publicly traded stocks are currently Oversold, Overbought or Neither</i>?

## Methodology
Our methodology to classify publicly traded stocks as overbought or oversold.
![Image of OSEMN](https://raw.githubusercontent.com/cousinskeeta/multi-class/master/OSEMN.png)

## Dataset
The dataset combines fundamental and indicator data for the publicly trades stocks predicting if the stocks are currently overbought or oversold, or neither. * This data was updated on 03/07/2020. )`Stock_Dataset_13.csv`

## Models
Support Vector Machine, Random Forest Classifier, KNN Classifier, Decision Tree Classifier, SGDClassifier, AdaBoost Classifier, Voting Classifier, Stacking Classifiers, and MLPClassifier.

## Shape
(1938, 29)

## Feautres
('current_price', 'prev_close', 'opens', 'bids', 'ask', 'day_range_min',
'day_range_max', 'fifty_two_wk_min', 'fifty_two_wk_max', 'volume',
'avg_volume', 'market_cap', 'beta', 'PE_ratio', 'eps',
'earnings_date_min', 'earnings_date_max', 'dividend_yield',
'dividend_date', 'one_year_est', 'RSI', 'Adj_Close', 'Change', 'Gain',
'Loss', 'AVG_gain', 'AVG_Loss', 'RS')
       
## Target
('target')

## PCA
![Image of Feature Correlation](https://raw.githubusercontent.com/cousinskeeta/multi-class/master/feature_correlation.png)
![Image of Priciple Component Correlation](https://raw.githubusercontent.com/cousinskeeta/multi-class/master/pca_features.png)

## Final Model
The comparison of all models against our baseline model shows us which model performed the best. This is done by assessing each model's test accuracy. By combining grid search and cross-validataion to fine tune our model, we now are able to accurately classify publicly traded stocks, based on ten principal component analysis instead of the original 29 in the dataset. We can choose from two of our top tuned models that share an accuracy score of 99.1%. 38% of oversold stocks were correctly classified. 60% of overbought stocks were also classified correctly. That gives us about 98% correctly classified based on the confusion matrix. We only have a 1.4% error rate of classification.

![Image of Priciple Component Correlation](https://raw.githubusercontent.com/cousinskeeta/multi-class/master/MLP_.png)


## Presentation:
https://docs.google.com/presentation/d/e/2PACX-1vSPp004EQo79AJujDohSZ8iJIDl7cSB1-hNDaB_3Hd0r48fvriVbRPiynXDINXZBuZPlXEKaGa5rq83/embed?start=true&loop=true&delayms=3000&slide=id.gc6f9e470d_0_24