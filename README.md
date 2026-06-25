# 🎯 Sentiment Analysis of Product Reviews

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange?logo=scikitlearn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

Binary sentiment classification (Positive / Negative) on real-world product, movie, and restaurant reviews, comparing three classic ML models end-to-end — from raw text to an interactive prediction demo.

---

## 📊 Dataset

**UCI Sentiment Labelled Sentences** — short, hand-labelled review sentences pulled from three different sources:

| Source | Domain |
|---|---|
| Amazon | Product reviews |
| IMDb | Movie reviews |
| Yelp | Restaurant reviews |

The notebook downloads the dataset automatically on first run, no manual setup required:
```
https://archive.ics.uci.edu/static/public/331/sentiment+labelled+sentences.zip
```

---

## 🧠 Models

| Model | Notes |
|---|---|
| Logistic Regression | Baseline linear classifier, also used for feature-importance analysis |
| Multinomial Naive Bayes | Fast probabilistic baseline well-suited to text |
| Random Forest | Non-linear ensemble for comparison |

Text is vectorized with **TF-IDF** (unigrams + bigrams) rather than raw counts, so the models can down-weight generic words (*"product"*, *"item"*) and up-weight strong sentiment signals (*"broken"*, *"fantastic"*, *"not good"*).

---

## 🔬 What's inside the notebook

1. **Install & imports** — auto-downloads the dataset
2. **Exploratory Data Analysis**
   - Class distribution
   - Word clouds (positive vs. negative)
   - Top-20 most frequent words by sentiment
   - Review length distribution
3. **Preprocessing** — text cleaning + TF-IDF vectorization (1–2 grams) with train/test split
4. **Model training** — Logistic Regression, Naive Bayes, Random Forest
5. **Evaluation**
   - Per-model metrics & confusion matrices
   - ROC-AUC curves
   - Comparative metrics table & charts
   - Feature importance (top predictive words)
6. **Interactive demo** — type any review and get a live Positive/Negative prediction with confidence score

---

## 🚀 Usage

```bash
git clone https://github.com/<your-username>/sentiment-analysis-product-reviews.git
cd sentiment-analysis-product-reviews
pip install -r requirements.txt  # or run the install cell in the notebook
jupyter notebook "sentiment_analysis code.ipynb"
```

Run all cells top to bottom — the dataset downloads automatically and every section (EDA → training → evaluation → demo) executes in order.

---

## 🛠️ Tech Stack

`numpy` · `pandas` · `matplotlib` · `seaborn` · `scikit-learn` · `nltk` · `wordcloud`

---

## 📁 Project Structure

```
.
├── sentiment_analysis code.ipynb   # main notebook (EDA → models → demo)
├── README.md
└── .gitignore
```
