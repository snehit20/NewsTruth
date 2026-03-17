# 📰 Fake News Detector for Local Languages

A **Machine Learning based Fake News Detection system** that classifies news headlines as **Real or Fake**.  
The system also supports **Hindi input**, automatically translating it into English before prediction.

This project demonstrates the use of **Natural Language Processing (NLP)** and **Machine Learning** techniques to detect misinformation.

---

# 1. 📌 Project Overview

Fake news spreads rapidly across social media platforms and digital news sources.  
This project aims to build a **binary text classification model** capable of identifying whether a news headline is:

• **Real News (Label = 1)**  
• **Fake News (Label = 0)**  

### Workflow of the System

1. Data loading and merging datasets  
2. Text preprocessing and cleaning  
3. Feature extraction using **TF-IDF**  
4. Training a **Logistic Regression model**  
5. Detecting language of input text  
6. Translating Hindi input to English  
7. Predicting whether the news is real or fake  

---

# 2. 🧠 Technologies Used

The following technologies and libraries were used in this project:

1. **Python**
2. **NumPy**
3. **Pandas**
4. **Matplotlib**
5. **Seaborn**
6. **NLTK**
7. **Scikit-learn**
8. **LangDetect**
9. **Translate API**

---

# 3. 📂 Dataset

The dataset contains two files:

1. **True.csv** → Real news articles  
2. **Fake.csv** → Fake news articles  

### Dataset Features

| Column | Description |
|------|-------------|
| title | News headline |
| text | Full news article |
| subject | Category of news |
| date | Publication date |

### Combined Dataset Information

1. Total samples → **808**
2. Real news → **405**
3. Fake news → **403**
4. Features → **Title, Text, Subject, Date**

---

# 4. ⚙️ Data Preprocessing

To prepare the text for machine learning, the following preprocessing steps were applied:

1. Convert text to **lowercase**
2. Remove **punctuation and numbers**
3. Remove **stopwords using NLTK**
4. Apply **Porter Stemming**
5. Generate cleaned text features

### Example

Original Title:
