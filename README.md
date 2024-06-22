# Stock-Sentiment-Analysis-using-Machine-Learning
# Stock Chosen: ETH-USD
# Introduction
The goal of this project is to predict stock price movements using machine learning. Specifically, we aim to determine whether the price of ETH-USD will go up or down on a given day based on historical data.

# Data Collection
I collected historical data for ETH-USD from 1st January 2021 to 31st December 2023. This data includes:

- Open price
- High price
- Low price
- Close price
- Adjusted close price
- Volume 

# Data for Testing
The testing data comprises the Open, High, Low, Close, Adjusted Close, and Volume for the following dates:

- April 2024: 15th, 20th, 23rd
- May 2024: 24th, 25th, 27th, 30th
- June 2024: 3rd-8th, 12th-14th, 17th-20th
  
# Data Preprocessing
Before feeding the data into the model, several preprocessing steps were undertaken:

## Data Cleaning
- Remove duplicates: Duplicate records (in terms of both historical data and news articles) were identified and removed to ensure each entry is unique.

## Check for Outliers
Outliers can significantly skew the results of the analysis. Therefore, checking and handling outliers is crucial.

- Identify outliers: IQR, a statistical method was used to identify outliers in the dataset.
- Handling outliers: Outliers were either removed or transformed depending on their impact on the analysis.

## Feature Engineering
- Create new features: New features such as daily_returns, pnl, and sentiment scores (ie subjectivity, polarity, positive, neutral, negative) from news articles were created to enhance the predictive power of the models.

# Model Building
For this project, I selected the LinearDiscriminantAnalysis (LDA) model, as a result of Cross Validation scores as compared to other classification models like LogisticRegression, SVC, RandomForestClassifier

## Model Training
The LDA model was trained using the preprocessed historical data. The target variable was labeled as follows:

- 1 represents that the price went up
- 0 represents that the price went down

# Resources used
- Yahoo Finance (https://finance.yahoo.com/quote/ETH-USD/news/)
- StockTwits (https://stocktwits.com/markets/news/crypto)
- Social media posts from Instagram and Twitter
- Google OCR
