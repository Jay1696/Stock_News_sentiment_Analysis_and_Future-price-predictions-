# Stock_News_sentiment_Analysis_and_Future-price-predictions

This report provides an overview of the code for performing stock news sentiment analysis, visualization, and prediction. The code consists of several sections that perform different tasks. Let's go through each section and understand its purpose.

**1. Loading Required Libraries:**

The code begins by importing the necessary libraries, including `urlopen` and `Request` from `urllib.request`, `BeautifulSoup` from `bs4`, `SentimentIntensityAnalyzer` from `nltk.sentiment.vader`, `pandas`, `matplotlib.pyplot`, and `datetime`.

**2. Scraping News Articles:**

The code prompts the user to enter a stock name and then scrapes news articles related to that stock from the "finviz.com" website using BeautifulSoup. It retrieves the HTML code and extracts the news article table.

**3. Parsing and Creating DataFrame:**

The code parses the data in the news table, extracts the ticker, date, time, and title of each article, and creates a DataFrame with this information.

**4. Sentiment Analysis:**

The code uses the VADER (Valence Aware Dictionary and sEntiment Reasoner) sentiment analysis tool from NLTK to analyze the sentiment of the news article titles. It calculates the sentiment scores (positive, negative, neutral, and compound) for each title and adds them to the DataFrame.

**5. Visualization:**

The code visualizes the sentiment scores by grouping them based on the ticker and date columns. It calculates the mean sentiment score for each date and plots a bar chart showing the sentiment trend over time.

**6. Sentiment Classification:**

The code classifies the sentiment of each news article title as positive, negative, or neutral based on the compound sentiment score. It adds a "Sentiment" column to the DataFrame with the corresponding classification.

**7. Visualization of Sentiment Distribution:**

The code calculates the percentage distribution of positive, negative, and neutral sentiments and visualizes it using a pie chart.

**8. Importing Stock Data:**

The code imports stock data using the `yfinance` library and downloads it to a CSV file named "stock.csv". It then reads the CSV file into a DataFrame.

**9. Stock Close Periods Visualization:**

The code plots a line chart to visualize the closing prices of the stock over a period of time.

**10. Stock Sentiment Visualization:**

The code plots a line chart to visualize the sentiment scores of the stock news articles over time.

**11. Data Preparation for Prediction:**

The code prepares the data for stock price prediction by selecting the required features and target variables. It creates a window of past data points and their corresponding sentiment scores.

**12. Scaling Data:**

The code scales the features and target variables using the MinMaxScaler from the `sklearn.preprocessing` module.

**13. Prediction using XGBoost Regressor:**

The code uses the XGBoost regressor from the `xgboost` library to train a model and make predictions on the test data. It evaluates the model's performance using metrics such as Root Mean Squared Error (RMSE) and R-squared.

**14. Visualization of Predicted vs. Real Stock Prices:**

The code visualizes the predicted and real stock prices using a line chart.

**15. Accuracy Calculation and Decision Tree Classification:**

The code calculates the accuracy of the predicted stock prices compared to the real prices. It also performs decision tree classification on the data to predict stock price movement.

**Conclusion:**

This code provides a comprehensive workflow for stock news sentiment analysis, visualization, and prediction. It scrapes news articles, performs sentiment analysis, visualizes sentiment trends, and predicts stock prices using XGBoost regressor and decision tree classification. The code offers valuable insights into stock market sentiment and can assist in making informed investment decisions.

Note: The code is presented as is, and improvements or modifications can be made to enhance its functionality and accuracy.
