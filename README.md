📰 Fake News Detector for Local Languages

A Machine Learning based Fake News Detection system that identifies whether a news headline is Real or Fake.
The model also supports Hindi input, automatically translating it to English before prediction.

This project demonstrates the use of Natural Language Processing (NLP) and Machine Learning for misinformation detection.

📌 Project Overview

Fake news spreads rapidly on social media and news platforms. This project aims to build a binary text classification model that can classify news headlines as:

Real News (1)

Fake News (0)

The system performs the following steps:

Data collection and preprocessing

Text cleaning and normalization

Feature extraction using TF-IDF

Training a Logistic Regression classifier

Detecting language and translating Hindi input

Predicting whether the news is real or fake

🧠 Technologies Used

Python

NumPy

Pandas

Matplotlib

Seaborn

NLTK

Scikit-learn

LangDetect

Translate API

📂 Dataset

The dataset consists of two files:

True.csv → Real news articles

Fake.csv → Fake news articles

Dataset features:

Column	Description
title	News headline
text	Full article text
subject	Category of news
date	Publication date

After merging both datasets:

Total samples: 808

Classes: Real (1), Fake (0)

⚙️ Data Preprocessing

Text preprocessing steps include:

Convert text to lowercase

Remove punctuation and numbers

Remove stopwords using NLTK

Apply Porter Stemming

Generate cleaned titles

Example:

Original Title:

BREAKING: Someone Else Connected To Trump Is Under Investigation

Cleaned Title:

break someon els connect trump investig
🔎 Feature Extraction

The project uses TF-IDF (Term Frequency - Inverse Document Frequency) to convert text into numerical vectors.

TfidfVectorizer(max_features=5000)

Output:

Dataset	Shape
Training	(646, 1849)
Testing	(162, 1849)
🤖 Model Used

Logistic Regression Classifier

Why Logistic Regression?

Efficient for text classification

Fast training

Works well with TF-IDF features

Strong baseline model

📊 Model Performance

Accuracy on test dataset:

Accuracy: 89.5%

Classification Report:

Class	Precision	Recall	F1-score
Fake News	0.88	0.91	0.89
Real News	0.91	0.88	0.90
🌍 Multilingual Support

The system supports Hindi input detection and translation.

Workflow:

Detect language using LangDetect

If Hindi detected:

Translate to English

Clean and vectorize text

Predict with trained model

Example:

Input: यह खबर बिल्कुल सही है और सरकार द्वारा जारी की गई है।
Output: Fake News
🧪 Example Predictions
predict_news("This is the official government website of India.")
→ Real News

predict_news("NASA confirms aliens are real and living in Canada!")
→ Fake News

📁 Project Structure
Fake-News-Detector
│
├── Fake.csv
├── True.csv
│
├── fake_news_detector.ipynb
│
├── README.md
│
└── requirements.txt
🚀 How to Run the Project
1️⃣ Clone the repository
git clone https://github.com/yourusername/fake-news-detector.git
2️⃣ Install dependencies
pip install -r requirements.txt
3️⃣ Run the notebook

Open the Jupyter Notebook:

fake_news_detector.ipynb
📦 Requirements

Example requirements.txt

numpy
pandas
matplotlib
seaborn
nltk
scikit-learn
langdetect
translate
🎯 Future Improvements

Possible improvements for the project:

Use full article text instead of titles

Train Deep Learning models (LSTM / BERT)

Support more languages

Deploy as a web application

Build a real-time fake news detection API

Use larger datasets

🌱 Research and Social Impact

This project aligns with UN Sustainable Development Goal 16:

Peace, Justice and Strong Institutions

Combating misinformation helps improve media transparency and public awareness.

👨‍💻 Author

Snehit Singh

B.Tech – Artificial Intelligence & Machine Learning
Interested in:

Machine Learning

NLP

AI for Social Good

Research in AI
