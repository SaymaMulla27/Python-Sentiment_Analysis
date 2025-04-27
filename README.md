# 📊 Sentiment Analysis using Python

## 📌 Overview

This project focuses on **Sentiment Analysis** using Python—a subfield of NLP that involves analyzing text data to determine the sentiment behind it. The aim is to calculate **sentiment polarity** (ranging from -1 to +1) and **subjectivity** (ranging from 0 to 1), helping us understand public opinion and emotions in text data, such as tweets.

Sentiment analysis is crucial for businesses to:
- Understand customer feedback
- Improve products and services
- Monitor public relations
- Gauge brand perception

---

## 📁 Dataset

We used tweet data extracted using **snscrape** and saved as a JSON file (`Sample Data.txt`), which we then converted into a CSV format for easier analysis.

---

## 🛠️ Libraries Used

```python
pandas, numpy, matplotlib, seaborn, wordcloud
nltk, textblob, re, string
snscrape (for data collection)
```

---

## 🔍 Data Preprocessing

To ensure high-quality sentiment insights, we performed several preprocessing steps:

- **Lowercasing**
- **Removing stopwords**
- **Stripping URLs, emojis, numbers, and punctuation**
- **Removing duplicate characters**
- **Removing short/meaningless words**
- **Tokenization** using `TweetTokenizer`
- **Stemming** using `PorterStemmer`
- **Lemmatization** using `WordNetLemmatizer`

---

## 🧠 Sentiment Calculation

Using the **TextBlob** library:

- **Polarity**: Measures how positive or negative a text is.
- **Subjectivity**: Measures how subjective (opinion-based) or objective (fact-based) a text is.

We created custom functions to extract these scores and added them as new columns to the dataframe.

---

## 🔄 Sentiment Labeling

Based on the polarity score:
- Score < 0 → **Negative**
- Score = 0 → **Neutral**
- Score > 0 → **Positive**

A new `analysis` column was added to reflect these labels for each tweet.

---

## 📊 Example Output

| content | polarity | subjectivity | analysis |
|--------|----------|--------------|----------|
| "thank popular sunday night pub quizzes..." | 0.38 | 0.46 | Positive |
| "without god week would sinday mournday..." | -0.37 | 0.62 | Negative |

---

## 📈 Future Improvements

- Incorporate advanced models like **VADER**, **BERT**, or **RoBERTa**.
- Visualize sentiment trends over time.
- Build a web dashboard using Streamlit or Flask.
- Train a custom classifier using machine learning.
