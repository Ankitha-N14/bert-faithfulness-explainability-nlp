# Improving Explainability in BERT-based NLP Models using Faithfulness Regularization

## Project Type

Research-based NLP Project (Manuscript Prepared)

---

## Overview

This project focuses on improving the interpretability of transformer-based NLP models, particularly BERT, by introducing a faithfulness-aware training mechanism.

Traditional explainability methods often highlight important tokens but fail to ensure that these tokens actually influence model predictions. This project addresses that gap by integrating explainability directly into the training process.

---

## Problem Statement

Modern NLP models such as BERT achieve high accuracy but lack transparency in decision-making.

Existing explainability techniques:

* Identify important tokens
* Do not guarantee that these tokens truly impact predictions

This project aims to:

* Improve faithfulness of explanations
* Align model predictions with highlighted tokens
* Build a more trustworthy NLP system

---

## Tech Stack

* Python
* PyTorch / Transformers (BERT)
* NumPy, Pandas
* Gradient-based attribution methods

---

## Datasets Used

* SST-2 (Sentiment Analysis)
* SNLI / E-SNLI (Natural Language Inference)
* HateXplain (Hate Speech Detection)

---

## Methodology

### Data Processing

* Tokenization using BERT tokenizer
* Input encoding (input IDs, attention masks)

### Model Architecture

* BERT-base (12-layer transformer encoder)
* Classification head using [CLS] token representation

### Explainability Approach

* Gradient × Input method for token importance scoring
* Token attribution based on embedding gradients

### Faithfulness Regularization

* Identified top important tokens
* Applied perturbation (masking tokens)
* Penalized model if prediction does not change significantly

### Loss Function

Combined objective:

* Cross-Entropy Loss (classification)
* Faithfulness Regularization Loss

---

## Evaluation Metrics

* Classification accuracy
* Prediction confidence change (deletion test)
* Faithfulness score based on token removal

---

## Results

* Model maintained strong performance across tasks
* Faithfulness improved through perturbation-based training
* Important tokens significantly impacted predictions after regularization

As observed in experiments :

* Sentiment task showed ~5.9% confidence drop after removing key tokens
* Hate speech task showed measurable reduction in prediction confidence
* Demonstrates improved alignment between explanations and predictions

---

## Key Contributions

* Introduced faithfulness-aware training for BERT-based models
* Integrated explainability directly into model optimization
* Improved reliability of token-level explanations
* Evaluated across multiple NLP tasks

---

## Limitations

* Experiments conducted on subset datasets
* Computational overhead due to perturbation
* No large-scale deployment

---

## Future Work

* Extend to larger datasets and real-time systems
* Apply to other transformer models (RoBERTa, GPT)
* Optimize computational efficiency of explanation methods

---

## Repository Structure

nlp-explainability-project
│
├── notebooks/
├── data/
├── models/
├── nlp_project.ipynb
└── README.md

---

## How to Run

pip install -r requirements.txt
python main.py

---

## Author

Ankitha Nambiar
Data Science Student
Interested in NLP, Explainable AI, and Machine Learning
