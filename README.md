# Basketball-Advanced-Stats-Web-Scraper

Web scraper developed by adapting scripts from [Medium Basketball Reference Article](https://medium.com/analytics-vidhya/intro-to-scraping-basketball-reference-data-8adcaa79664a) based on knowledge of Python, pandas, web scraping. 

Pulled Advanced Basketball Stats from years 1990-2020 from links in format:
https://www.basketball-reference.com/leagues/NBA_{year}.html (Example: https://www.basketball-reference.com/leagues/NBA_2021.html)

A testing dataset was then collected using data from the NBA 2022 regular season. 

Using an Artificial Neural Network in TensorFlow with Batch Normalization, Dropout, and several class imbalance techniques including oversampling, we then developed a model using the training data and predicted on the 2022 testing data. The model predicts the Miami Heat, Phoenix Suns, and Golden State Warriors as the most likely teams to win the 2022 championship (probability of winning > 0.5), with the Heat having the highest probability, such that they are the model's predicted champion. 

The visualizations and class imbalance techniques used in the ANN Notebook are based on the [TensorFlow Core Tutorial on Working with Class Imbalance](https://www.tensorflow.org/tutorials/structured_data/imbalanced_data)

