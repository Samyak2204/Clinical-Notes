# Clinical Notes NLP Pipeline

A simple NLP pipeline for **medical clinical notes**: text cleaning, exploratory analysis, classification, topic modeling, clustering, and summarization.  

---

## Features

- De-identify and clean clinical notes  
- TF-IDF vectorization (unigrams + bigrams)  
- Train **Naive Bayes** & **Logistic Regression** classifiers  
- Topic modeling with **LDA**  
- Clustering using **TF-IDF + SVD + Agglomerative Clustering**  
- Summarization using **facebook/bart-large-cnn**  
- Save cleaned data, models, and predictions  

---

## Dataset

- CSV file with at least:  
  - `TEXT` → clinical note text  
  - `DIAGNOSIS` → label for classification (optional)  

Update `DATA_PATH`, `TEXT_COL`, `LABEL_COL` in the notebook as needed.  

---

## Usage

1. Install dependencies:

```bash
pip install -r requirements.txt
```
2.	Run Clinical_Notes_Pipeline.ipynb sequentially:
```bash
•	Load data → clean → EDA → TF-IDF → classification → LDA → clustering → summarization → save artifacts
```
3.	Outputs saved:
```bash
•	Cleaned notes: clinical_notes_cleaned.csv
•	Models: nb_model.pkl, lr_model.pkl
•	Vectorizer: tfidf_vectorizer.pkl
•	Predictions: predictions_tfidf_lr.csv
```
