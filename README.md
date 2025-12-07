# SMS Spam Classifier – End-to-End Machine Learning Project

## Overview
This project is an end-to-end implementation of an SMS Spam Classifier that detects whether a message is spam or ham. The pipeline includes data cleaning, exploratory data analysis, text preprocessing, model training, evaluation, improvements, website creation, and deployment. The final selected model uses TF-IDF vectorization with Multinomial Naive Bayes.

---

## Project Workflow
1. Data Cleaning  
2. Exploratory Data Analysis (EDA)  
3. Text Preprocessing  
4. Model Building  
5. Model Evaluation  
6. Improvement Attempts  
7. Streamlit Website Development  
8. Deployment  

---

## Dataset Description
The SMS Spam Collection Dataset contains **5,574** English SMS messages labeled as **ham** (legitimate) or **spam**.

Each row has two columns:
- **v1**: label (ham/spam)
- **v2**: raw SMS text

### Dataset Sources
The dataset combines messages from:
- Grumbletext Web Forum (425 spam messages)  
- NUS SMS Corpus (3,375 ham messages)  
- Caroline Tag’s PhD thesis (450 ham messages)  
- SMS Spam Corpus v0.1 Big (1,002 ham, 322 spam)

Original dataset:  
http://www.dt.fee.unicamp.br/~tiago/smsspamcollection/

Recommended citation:  
Almeida, T.A., Hidalgo, J.M.G., Yamakami, A. (2011). Contributions to the Study of SMS Spam Filtering. ACM DOCENG'11.

---

## Technologies Used
**Libraries:**
- numpy  
- pandas  
- nltk  
- scikit-learn  
- xgboost  
- streamlit  

**NLP & ML Tools:**
- TF-IDF Vectorization  
- Multinomial Naive Bayes  
- Logistic Regression  
- SVC  
- Decision Tree  
- KNN  
- Random Forest  
- Extra Trees  
- AdaBoost  
- Bagging  
- Gradient Boosting  
- XGBoost  
- Voting Classifier  
- Stacking Classifier  

---

## Exploratory Data Analysis (EDA)
EDA was performed to examine:
- Spam vs ham distribution  
- Message lengths and statistics  
- Frequent words  
- Visualization through plots and word clouds  

---

## Text Preprocessing
Steps applied:
1. Lowercasing  
2. Tokenization  
3. Removing special characters  
4. Removing stopwords  
5. Stemming (NLTK)  
6. TF-IDF vectorization  

---

## Model Development
Multiple models were trained and compared.  
The final selected configuration:

- **Vectorizer:** TfidfVectorizer  
- **Model:** MultinomialNB  

---

## Model Evaluation
Performance of Multinomial Naive Bayes:
Accuracy: 0.9719

Confusion Matrix:
[[896 0]
[ 29 109]]

Precision: 1.0


Reasons for selection:
- Highest precision (no false positives)
- Competitive accuracy
- Fast and efficient for sparse text data

---

## Model Improvement Attempts
Several enhancements were attempted but did not improve accuracy or precision:

- MinMaxScaler  
- Adding engineered feature: num_characters  
- Voting Classifier (SVC, MNB, Extra Trees)  
- Stacking Classifier (RandomForest as meta-learner)  

MultinomialNB remained the best-performing model.

---

## Web Application
A Streamlit web application was created that:
- Accepts user SMS input  
- Applies preprocessing  
- Predicts spam or ham using the saved model  
- Displays results in a simple UI  

---

## Deployment
The application was deployed (Streamlit Cloud or similar):

- Model saved using pickle  
- TF-IDF vectorizer saved and loaded at runtime  
- Streamlit app connected to backend model  

---

## Results
- Final Model: **Multinomial Naive Bayes**  
- Accuracy: **97.19%**  
- Precision: **100%**  
- Outperformed all ensemble and stacking techniques tested  

---

## References
Dataset:  
http://www.dt.fee.unicamp.br/~tiago/smsspamcollection/
