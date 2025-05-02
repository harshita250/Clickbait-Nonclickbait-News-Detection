# 📰 Clickbait Detection in News Headlines

This repository contains the full pipeline for detecting clickbait in news headlines using machine learning and natural language processing. The project was developed as part of a team effort to explore and understand the linguistic, structural, and semantic patterns behind clickbait content.

---

## 📌 Problem Statement

Clickbait headlines are designed to attract clicks but often mislead readers. The goal of this project is to automatically detect such headlines using data-driven techniques and improve content transparency and user experience on digital platforms.

---

## 🧠 Research Questions

- What linguistic features distinguish clickbait from non-clickbait?
- Which machine learning model performs best for this classification task?
- How can misclassified headlines be better understood and reduced?
- What practical applications can clickbait detection offer in real-world platforms?

---

## 🗃️ Dataset

- **Training Data**: 32,000 labeled headlines from a mix of clickbait-heavy and reputable sources.
- **Testing Data**: Curated from BuzzFeed (clickbait) and BBC/Fox News (non-clickbait).
- **Sources include**: BuzzFeed, Upworthy, WikiNews, The Guardian, New York Times, The Hindu.

---

## 🛠️ Methodology

### 🧹 Data Preprocessing
- Lowercasing, punctuation removal
- Stopword removal, lemmatization
- Sentiment tagging using `TextBlob` and `NLTK`
- Named Entity Recognition with spaCy
- POS tagging and feature extraction (e.g., use of numbers, personal pronouns)

### 📊 Exploratory Data Analysis
- Distribution of headline lengths, sentiment, POS usage
- TF-IDF scoring and word clouds
- Readability scores: Flesch-Kincaid, Gunning Fog, Coleman-Liau
- Statistical tests (t-test, Mann-Whitney U) to confirm feature significance

### 🔍 Feature Engineering
- Binary flags: `contains_numbers`, `contains_personal_pronouns`, `contains_gpe`
- Sentiment polarity scores
- Custom features from NER and POS analysis

### 🧪 Modeling Techniques
- TF-IDF vectorization for headline text
- Classification algorithms:
  - Logistic Regression
  - Random Forest
  - Multinomial Naive Bayes

---

## 🧾 Results

| Model                     | Accuracy (Baseline) | Accuracy (With Features) |
|--------------------------|---------------------|---------------------------|
| Logistic Regression      | 56.4%               | **82.81%**                |
| Random Forest            | 83.0%               | **87.01%**                |
| Multinomial Naive Bayes  | 68.0%               | **84.56%**                |

---

## 📉 Topic & Semantic Analysis
- LDA topic modeling to identify dominant themes in both classes
- t-SNE on spaCy embeddings to visualize semantic separation between categories

---

## 🔍 Misclassification Insights

- Ambiguous language and emotional context contribute to misclassifications.
- Headlines sharing structural similarities with both classes were often wrongly predicted.
- Some errors stem from evolving clickbait tactics.

---

## 🌍 Real-World Applications

- Improving content recommendation systems
- Enhancing editorial integrity in newsrooms
- Flagging misleading content in social platforms
- Supporting digital literacy tools for users

---

## 📈 Future Work

- Add real-time streaming clickbait detection
- Include visual/multimodal analysis (thumbnails, emojis)
- Integrate feedback loops for model retraining
- Localize models to account for regional language patterns

---

## 📚 References

- Potthast et al. (2016), West & Chang (2016), Chakraborty (2020)
- NLP libraries: spaCy, TextBlob, NLTK
- Classifiers: scikit-learn, CountVectorizer, TF-IDF


