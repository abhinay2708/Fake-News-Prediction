📰 Fake News Detection using NLP & Deep Learning
📌 Project Overview

Fake news has become one of the biggest challenges in today’s digital era. Social media platforms and online news portals often spread misinformation that can influence public opinion and decision-making.

This project focuses on building a Fake News Detection system that leverages Natural Language Processing (NLP) and Deep Learning to automatically classify news articles as real or fake.

The approach includes data preprocessing, exploratory data analysis (EDA), feature engineering, and building a sequence model (LSTM) to capture contextual meaning in text data.

📊 Dataset Details

Total Records: ~44,000 articles (balanced between fake and real)

Features:

title → headline of the article

text → complete article content

subject → category of article (e.g., politics, world news)

date → date of publication

target → label (1 = Real, 0 = Fake)

Data Preparation Steps:

Combined title + text to get more context.

Removed HTML tags, punctuation, numbers, and special characters.

Lowercased all words.

Removed stopwords using NLTK.

Applied lemmatization to normalize words.

Tokenized text and padded sequences for uniform input size.

🔍 Exploratory Data Analysis (EDA)

Class balance: Almost equal distribution of fake and real news (no imbalance).

Subject distribution: Most articles were related to politics and world news.

Word frequency: Top keywords included Trump, Russia, government, Clinton.

Text length distribution: Real news articles were generally longer than fake ones.

🧠 Model Architecture

A deep learning LSTM model was implemented:

Embedding Layer

Converts word indices into dense vector representations.

Embedding dimension: 100.

LSTM Layers

Stacked Bidirectional LSTMs for sequential learning.

Captures long-term dependencies and context.

Dropout Layers

Used to reduce overfitting (dropout rate = 0.3).

Dense Output Layer

Fully connected layer with sigmoid activation for binary classification.

⚙️ Model Training Setup

Loss Function: Binary Crossentropy

Optimizer: Adam (lr = 0.001)

Batch Size: 32

Epochs: 30 (with EarlyStopping)

Validation Split: 20%

📈 Results

Training Accuracy: 98.17%

Testing Accuracy: 97.9%

Validation Loss Curve: Showed convergence with minimal overfitting.

💡 Key Learnings

Proper preprocessing (lemmatization, stopword removal) significantly boosts NLP model accuracy.

LSTMs outperform simple feed-forward models for sequential text tasks.

Balanced datasets make the model more generalizable.

Fake news detection benefits from combining EDA insights with deep learning.
