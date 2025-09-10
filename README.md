# Fake-news-classification

## Overview
This project aims to classify news articles as **REAL** or **FAKE** using Natural Language Processing (NLP) and Machine Learning. The pipeline includes text preprocessing, feature extraction, model training, evaluation, and interpretability.


## Dataset
- Contains news articles with two columns:
  - `text`: News content
  - `label`: `REAL` or `FAKE`
- Class distribution checked for balance.
- Text length distribution analyzed.


## Preprocessing
- Lowercasing text
- Removing URLs, emails, special characters
- Tokenization & stopword removal
- Lemmatization  
**Example:**

"Breaking news: President visits the city!" → "breaking news president visit city"
  
## Feature Extraction
- TF-IDF vectorization (max 20,000 features)
- Unigrams + Bigrams
- Train-test split: 75% training, 25% testing


## Models
- **Logistic Regression** (class_weight='balanced', max_iter=1000)  
- **Multinomial Naive Bayes**  
- **Linear SVM** (class_weight='balanced')

**Evaluation Metrics:**  
- Accuracy  
- Precision  
- Recall  
- F1-score  
- Confusion Matrix  
- ROC-AUC Curve


## Model Interpretability
- **LIME** used to explain predictions
- Highlights words contributing to a classification


## Results
- Logistic Regression & SVM perform best
- ROC curves indicate high TPR with low FPR
- LIME explanations provide insight into model decisions




