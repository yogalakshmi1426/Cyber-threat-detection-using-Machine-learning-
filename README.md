# 🛡️ Cyber Threat Detection using Machine Learning

> MSc Dissertation — University of Sussex — Distinction (99.6% Accuracy)

A machine learning pipeline that automatically detects cyber threats 
from real network traffic data — distinguishing between normal activity 
and botnet attacks with 99.6% accuracy across 18,443 test samples.

---

## Results

| Metric | Score |
|--------|-------|
| Accuracy | **99.6%** |
| Precision | 0.997 |
| Recall | 0.996 |
| F1-Score | 0.996 |
| Test Samples | 18,443 |

---

## The Problem

Traditional rule-based security systems fail against novel attack 
patterns — they only catch threats they have already seen.

This project built a machine learning pipeline that learns what 
normal network traffic looks like, then flags anything that deviates 
from it — catching attacks that rule-based systems would miss entirely.

---

## Dataset

**CTU-13 Dataset** — Real botnet traffic captured at Czech Technical 
University. Contains genuine attack traffic mixed with normal activity.

This is not a synthetic or toy dataset. These are real network packets 
from real botnet attacks, making the results directly applicable to 
production security environments.


'''
Raw Network Traffic
↓
Data Cleaning + Preprocessing (pandas)
↓
Class Imbalance Fix (SMOTE oversampling)
↓
Feature Standardisation (StandardScaler)
↓
Dimensionality Reduction (PCA)
↓
Random Forest Classifier
↓
99.6% Accuracy on 18,443 test samples
'''
---

## Why Random Forest?

Random Forest was selected after comparing multiple classifiers because:
- Handles high-dimensional network traffic features well
- Robust to outliers in packet timing and size data
- Provides feature importance scores for interpretability
- Resistant to overfitting on imbalanced security datasets

---

## Key Technical Decisions

**SMOTE** — The dataset had far more normal traffic than attack traffic. 
Without correction, the model would learn to predict "normal" for 
everything and still appear 90%+ accurate. SMOTE created synthetic 
attack samples to balance the classes before training.

**PCA** — Network traffic data has many correlated features. PCA reduced 
dimensionality while preserving variance, speeding up training without 
sacrificing accuracy.

**StandardScaler** — Network features like packet size and timing operate 
on very different scales. Standardisation ensures no single feature 
dominates the model due to its unit of measurement.

---

## Results by Class

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| Normal Traffic | 0.998 | 0.997 | 0.997 | 12,847 |
| Attack Traffic | 0.994 | 0.996 | 0.995 | 5,596 |
| **Overall** | **0.997** | **0.996** | **0.996** | **18,443** |

---

## Tools and Technologies

Python · scikit-learn · pandas · NumPy · SMOTE (imbalanced-learn) · 
PCA · StandardScaler · Random Forest · Matplotlib · Seaborn

---

## What I Would Add With More Time

1. Real-time stream processing — detect threats as packets arrive 
   rather than in batch mode
2. Explainability layer — SHAP values showing which features triggered 
   each alert
3. Drift detection — flag when incoming traffic patterns shift away 
   from training data (links to my Silent ML Failure Detection project)

---

## About

MSc Computer Science dissertation submitted to University of Sussex.
Grade: Distinction
Uploaded for portfolio and job reference purposes only.

**Author:** Yogalakshmi Shanmuga Jothi  



---

## Pipeline
