# Sentiment Analysis of SMS Chat Messages
This project performs sentiment analysis on messages from the NUS SMS Corpus dataset. The goal is to classify text into Positive or Negative sentiment, visualize the distribution of sentiment across countries, and explore how communication varies globally.

## Table of Contents:
- Overview
- Dataset
- Requirements
- Data Preprocessing
- Exploratory Data Analysis (EDA)
- Sentiment Analysis
- Visualization
- Results
- Conclusion
  
### Overview:
##### The purpose of this project is to use Natural Language Processing (NLP) techniques to:
Preprocess the message text to remove unwanted data such as URLs, HTML tags, punctuation, and unnecessary characters.
Analyze the sentiment of each message, categorizing it into either Positive or Negative sentiment.
Compare the general sentiment of messages between different countries.

### Dataset:
The dataset used for this project is the NUS SMS Corpus, which contains over 48,500 SMS messages from users across various countries.

### Requirements:
To run this project, you need the following libraries:

-npandas: Data manipulation and analysis.
-nnltk: Natural Language Processing.
- matplotlib: Plotting and visualization.
- seaborn: Statistical data visualization.
- re: Regular expressions for text cleaning.

### Data Preprocessing:
We performed the following steps to clean and prepare the dataset:

- Remove Empty Messages: Dropped rows with null values in the message column.
- Lowercasing: Converted all messages to lowercase.
- Remove Punctuation: Removed all punctuation marks using regular expressions.
- Remove URLs: Stripped out any URLs present in the messages.
- Remove HTML Tags: Removed HTML tags.
- Tokenization: Split the cleaned message data into individual tokens (words).

### Exploratory Data Analysis (EDA):
Before building the sentiment analysis model, we performed exploratory data analysis (EDA) to get insights into the dataset:

- Country Distribution: The dataset contains messages from various countries, with the majority of messages coming from Singapore, India, and USA.
(We visualized the distribution of messages per country using a horizontal bar plot)

### Sentiment Analysis:
- Model Selection:
We used the Naive Bayes Classifier from the nltk library to classify messages as Positive or Negative. The classifier was trained using tokenized Twitter data as labeled samples.
- Key Steps in Sentiment Analysis:
* Tokenization: Tokenized the SMS messages using nltk.word_tokenize().
* Feature Extraction: Created a frequency distribution of common words in positive and negative tweets.
* Training: Built a Naive Bayes model with 70% of the dataset used for training and 30% for testing.
* Prediction: Classified the sentiment of each SMS message.
* Model Accuracy: The Naive Bayes model achieved an accuracy of ~85% on the test set.

### Visualization:
After performing sentiment analysis, we visualized the results:
- Overall Sentiment Distribution: Displayed the overall proportion of Positive and Negative messages in the dataset using a countplot.

### Results:
58.60% of the messages in the dataset were classified as Negative, and 41.40% as Positive.
Singapore, India, and USA had the highest number of messages.
Sentiment scores by country reveal which countries send more positive or negative messages on average.

### Conclusion:
This project demonstrates how Natural Language Processing techniques can be applied to SMS datasets for sentiment analysis. Using a Naive Bayes classifier, we were able to classify messages and explore how sentiment differs between countries.

### The next step could be to:
Improve the model by using deep learning techniques.
Expand the analysis to include more granular sentiment categories, such as Neutral, or emotion-based labels like Happy, Angry, etc.

##### Feel free to contribute to this project by submitting issues or pull requests!
