# AI-Powered Customer Issue Intelligence (NLP)
## Project Artifacts
- 📘 [Main Analysis Notebook][![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](
https://colab.research.google.com/github/sushmitha-lab/AI-powered-customer-issue-intelligence/blob/main/notebooks/01_complaint_nlp_analysis.ipynb
)


## Overview
This project builds an end-to-end NLP system to analyze and classify real-world consumer complaint narratives into financial product categories.

The solution compares classical NLP techniques with transformer-based models and highlights real-world challenges such as class imbalance, label ambiguity, and long-form unstructured text.

---

## Business Problem
Financial institutions receive large volumes of customer complaints written in free-form text.  
Manual triage is slow, inconsistent, and difficult to scale.

This project demonstrates how NLP can be used to:
- Automatically classify complaints by product
- Identify ambiguous and overlapping complaint categories
- Support customer experience and risk analysis teams

---

## Dataset
**Consumer Complaint Database (CFPB)**

- 230,000+ real consumer-written complaints
- Long-form, unstructured narratives
- Multiple financial products and issue categories
- Highly imbalanced and noisy labels

---

## Approach

### 1. Data Understanding & NLP-Specific EDA
- Filtered non-empty complaint narratives
- Analyzed text length distribution and class imbalance
- Identified label explosion and reframed classification at the product level

### 2. Baseline NLP Model
- TF-IDF vectorization with Logistic Regression
- Macro F1 used as primary evaluation metric
- Strong baseline performance on frequent product categories

### 3. Transformer-Based Modeling
- Sentence-BERT embeddings for semantic representation
- Logistic Regression classifier on dense embeddings
- Compared performance tradeoffs against TF-IDF baseline

### 4. Error Analysis & Insights
- Confusion matrix analysis
- Manual inspection of misclassified complaints
- Identified label ambiguity and multi-product narratives

---

## Results
- TF-IDF baseline achieved strong macro F1 performance on frequent categories
- Transformer model improved semantic understanding for complex products such as mortgages, student loans, and debt collection
- Both models struggled on highly ambiguous and low-support categories, reflecting real-world data challenges

---

## Key Insight
Classical NLP models provide robust baselines for large-scale text classification, while transformer-based models enhance semantic understanding but remain sensitive to label noise and sample imbalance.

---

## Tools & Technologies
Python, pandas, scikit-learn, Sentence-BERT, NLP, Machine Learning, Google Colab
