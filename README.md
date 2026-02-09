# AraBERT Token Classification – Arabic ABSA

This project fine-tunes **AraBERT (aubmindlab/bert-base-arabertv2)** for Arabic token classification using the Hugging Face Transformers library. The task is similar to Named Entity Recognition (NER) and is applied to Aspect-Based Sentiment Analysis (ABSA).

## Project Overview

The project implements an end-to-end NLP pipeline for sequence labeling in Arabic, including:

- Loading labeled data from an Excel file  
- Preprocessing and grouping tokens into sentences  
- Encoding aspect labels into numerical IDs  
- Tokenization using AraBERT tokenizer  
- Aligning labels with subword tokens  
- Training a token classification model  
- Evaluating performance using seqeval metrics  
- Running predictions on new Arabic sentences  

---

## Model

- **Pretrained Model:** `aubmindlab/bert-base-arabertv2`  
- **Task:** Token Classification  
- **Evaluation Metrics:**  
  - Precision  
  - Recall  
  - F1-score  
  - Accuracy  

---

## Dataset Format

The input Excel file must contain at least the following columns:

| Sentence # | word | aspect |
|------------|------|--------|
| 1          | الأكل | B-FOOD |
| 1          | ممتاز | O |

Each row represents a token and its corresponding label.

---

## Inference Example :
The notebook includes a function to test new sentences such as:
  -"الأكل كان ممتاز لكن خدمة التوصيل سيئة"
  -"المكان كان جيد لكن الاستقبال سيء"
  The model predicts aspect tags for each token.

---

## Author :
**Mohammad Ali Othman**
Data Science Student
Jordan University of Science and Technology
