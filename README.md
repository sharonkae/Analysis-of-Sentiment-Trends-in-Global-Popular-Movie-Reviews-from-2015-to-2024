# Analysis-of-Sentiment-Trends-in-Global-Popular-Movie-Reviews-from-2015-to-2024

This project analyzes IMDB movie reviews using multiple sentiment analysis approaches, compares their performance, and visualizes insights through an interactive Streamlit dashboard.  
The workflow includes data cleaning, exploratory data analysis (EDA), NLP preprocessing, three sentiment models (VADER, BERT, ML), and dashboard deployment.

---

## Project Proposal

The goal of this project is to understand how audiences react to movies by analyzing large-scale IMDB reviews.  
Specifically, the project aims to:

1. Clean and preprocess two datasets:
   - **Movie metadata** (title, year, genre, rating)
   - **IMDB reviews** (review text, rating, sentiment labels)
2. Perform **EDA** to explore rating trends, genre patterns, and review characteristics.
3. Apply **three sentiment analysis methods**:
   - **VADER** (rule-based)
   - **BERT** (transformer-based deep learning)
   - **Traditional ML model** (Logistic Regression / SVM)
4. Compare the performance of the three models.

---

## Steps Taken

### 1. Data Cleaning
Both datasets were cleaned independently before merging:
- Removed duplicates
- Standardized column names
- Converted data types (ratings, year)
- Cleaned review text (lowercasing, removing HTML, punctuation, whitespace)
- Removed extremely short reviews
- Split movie genres into lists
- Merged datasets using `imdb_id`

### 2. Exploratory Data Analysis (EDA)
EDA was performed on both datasets:
- Rating distribution
- Movies per year
- Genre frequency
- Review length distribution
- TF-IDF keywords
- WordCloud visualization
- Sentiment distribution

### 3. Sentiment Analysis Models
Three models were implemented:

#### VADER  
A lexicon-based model suitable for social media and short reviews.  
Output stored in:
- `sentiment_score`
- `sentiment_label`

#### BERT  
A transformer-based classifier fine‑tuned for sentiment analysis.  
Output stored in:
- `bert_label`
- `bert_binary`
- `bert_confidence`

#### Machine Learning Model  
A traditional ML classifier trained on TF-IDF features.  
Output stored in:
- `ml_pred`
- `ml_label`

### 4. Model Comparison
For each year, the average sentiment score was computed:
- `vader_avg`
- `bert_avg`
- `ml_avg`


