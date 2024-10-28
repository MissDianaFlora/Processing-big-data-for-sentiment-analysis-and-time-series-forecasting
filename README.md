# LSTM AND AUTOREGRESSIVE TIME SERIES FORECASTING OF SENTIMENTS AT DAY 1,3 AND 7 GOING FOWARD

This project focuses on building a comprehensive sentiment forecasting pipeline for tweets using LSTM and autoregressive (AR) models, incorporating big data processing, storage, and sentiment analysis. Key processes include data collection, storage, sentiment extraction, vectorization, database benchmarking, and model training.

# Key Processes:

## 1. Data Ingestion: Tweets are collected in real-time to capture shifting sentiments accurately.
Storage in MongoDB and MySQL: MongoDB, a NoSQL database, is used to store large volumes of unstructured tweet data efficiently, while MySQL provides a structured baseline for database performance comparisons.
Sentiment Extraction and Analysis:

## 2. Text Processing: The text of tweets is preprocessed to remove noise and prepare for sentiment analysis.

## 3. Sentiment Extraction: Two sentiment analysis methods are used:
- TextBlob for language translation and lexicon-based analysis, which calculates polarity and subjectivity.
- VADER for handling social media-specific text features like emojis, slang, and abbreviations, allowing for quick rule-based analysis.
- Vectorization: The processed text is converted into numerical matrices using TF-IDF Vectorizer and CountVectorizer, transforming the text into structured input for machine learning models.

## 4. Database Benchmarking with YCSB:
YCSB Benchmarking: Using Yahoo Cloud Serving Benchmark (YCSB), MongoDB and MySQL are evaluated for performance under varied data sizes, request distributions, and workloads. This helps to identify the optimal database setup for efficient big data processing.

## 5. Sentiment Classification and Model Training:
Multinomial Naïve Bayes Classification: After vectorization, the tweet data is split into training and test sets for classification using a Multinomial Naïve Bayes model.

## 6. Time Series Modeling with LSTM and AR: The sentiment data is structured as a time series and used to train LSTM and AR models for forecasting sentiments at day 1, day 3, and day 7 horizons.
