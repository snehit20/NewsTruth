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

1. Python
2. NumPy
3. Pandas
4. Matplotlib
5. Seaborn
6. NLTK
7. Scikit-learn
8. LangDetect
9. Translate API

---

# 3. 📂 Dataset

The dataset contains two files:

1. **True.csv** → Real news articles
2. **Fake.csv** → Fake news articles

### Dataset Features

| Column  | Description       |
| ------- | ----------------- |
| title   | News headline     |
| text    | Full news article |
| subject | Category of news  |
| date    | Publication date  |

### Combined Dataset Information

1. Total samples → **808**
2. Real news → **405**
3. Fake news → **403**
4. Features → **Title, Text, Subject, Date**

---

# 4. ⚙️ Data Preprocessing

To prepare the text for machine learning, the following preprocessing steps were applied:

1. Convert text to lowercase
2. Remove punctuation and numbers
3. Remove stopwords using NLTK
4. Apply Porter Stemming
5. Generate cleaned text features

### Example

Original Title:

BREAKING: Someone Else Connected To Trump Is Under Investigation

Cleaned Title:

break someon els connect trump investig

---

# 5. 🔎 Feature Extraction

Text data cannot be used directly in machine learning models.
Therefore, **TF-IDF (Term Frequency – Inverse Document Frequency)** is used to convert text into numerical vectors.

### TF-IDF Configuration

TfidfVectorizer(max_features = 5000)

### Dataset Shapes After Vectorization

1. Training data → **(646, 1849)**
2. Testing data → **(162, 1849)**

---

# 6. 🤖 Machine Learning Model

The project uses the **Logistic Regression algorithm** for classification.

### Reasons for using Logistic Regression

1. Works well for text classification
2. Fast and efficient
3. Performs well with TF-IDF features
4. Provides strong baseline performance

---

# 7. 📊 Model Performance

### Accuracy

Accuracy: **0.895**

### Classification Report

| Class     | Precision | Recall | F1-Score |
| --------- | --------- | ------ | -------- |
| Fake News | 0.88      | 0.91   | 0.89     |
| Real News | 0.91      | 0.88   | 0.90     |

### Observations

1. The model achieves approximately **89% accuracy**
2. Precision and recall values are balanced
3. The classifier performs well for both classes

---

# 8. 🌍 Multilingual Support

The model also supports **Hindi language input**.

### Process

1. Detect language using **LangDetect**
2. If language is Hindi:

   * Translate text to English
3. Apply preprocessing
4. Convert text using TF-IDF
5. Predict using the trained model

---

# 9. 🧪 Example Predictions

### Example 1

Input:

This is the official government website of India.

Output:

Real News

---

### Example 2

Input:

यह खबर बिल्कुल सही है और सरकार द्वारा जारी की गई है।

Output:

Fake News

---

### Example 3

Input:

NASA confirms aliens are real and living in Canada!

Output:

Fake News

---

# 10. 📁 Project Structure

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

---

# 11. 🚀 How to Run the Project

### Step 1 — Clone the Repository

git clone https://github.com/yourusername/fake-news-detector.git

### Step 2 — Install Dependencies

pip install -r requirements.txt

### Step 3 — Run the Notebook

Open the Jupyter notebook:

fake_news_detector.ipynb

Run all cells to train the model and test predictions.

---

# 12. 📦 Requirements

Example requirements.txt

numpy
pandas
matplotlib
seaborn
nltk
scikit-learn
langdetect
translate

---

# 13. 🔮 Future Improvements

Possible improvements for this project include:

1. Using full article text instead of only titles
2. Implementing Deep Learning models (LSTM / BERT)
3. Supporting more languages
4. Deploying the model as a web application
5. Creating a real-time fake news detection API
6. Training on larger datasets

---

# 14. 🌱 Social Impact

This project contributes to combating misinformation and aligns with:

**UN Sustainable Development Goal 16 — Peace, Justice and Strong Institutions**

Detecting fake news helps improve **information reliability and media transparency**.

---

# 15. 👨‍💻 Author

**Snehit Singh**
B.Tech — Artificial Intelligence & Machine Learning

Interests:

• Machine Learning
• Natural Language Processing
• AI for Social Good
• Artificial Intelligence Research
