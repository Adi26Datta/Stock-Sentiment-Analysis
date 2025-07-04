# Stock Sentiment Analysis – Meta (Facebook)

This project performs sentiment analysis on **Meta (Facebook)** news headlines to predict **buy/sell signals** using machine learning. It uses **NYTimes API** for news and **Yahoo Finance** for historical stock data, combines them, and applies feature engineering and model training.

---

## Project Structure

### Notebook 1

* Fetches Meta headlines from the NYTimes Archive API

* Retrieves historical Meta stock data using yfinance

* Cleans and preprocesses headlines (tokenization, stopword removal, etc.)

* Merges news and stock info into a single clean dataset

* Saves it as merged.csv

---

### Notebook 2: 

* Loads `merged.csv`
* Extracts features using **TF-IDF**
* Runs multiple classifiers :
  * Support Vector Classifier
  * Logistic Regression
  * Random Forest
  * Gradient Boosting, AdaBoost, etc.
* Uses GridSearchCV to find best hyperparameters
* Combines top models in a **VotingClassifier**
* Predicts buy/sell signals
* **Plots** predicted vs actual signals on stock price chart for visual insight

---

### Data Files: 

* facebook_news.csv: Raw headlines from NYTimes
* merged.csv: Final merged dataset for modeling
* final dataset.csv: Possibly filtered or enriched dataset

---
## Output

* Final model outputs:

  * Accuracy, Precision, Classification Report
  * Buy/Sell prediction plotted on Meta's stock price graph
* Helps visualize sentiment-driven entry/exit points

---

## How to Run

```bash

# Run each notebook step-by-step
1. Run notebook1 to generate `merged.csv`
2. Run notebook2 for training, prediction, and visualization
```

---

## Future Ideas

* Add deep learning (e.g., LSTM, FinBERT)
* Improve stock-sentiment alignment using event-based labeling
* Incorporate volume or technical indicators

---
