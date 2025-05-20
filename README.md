# Smart Audit Claim Prediction with AI & Azure

This repository contains an advanced pipeline for healthcare claim audit analysis using feature engineering and Azure OpenAI embeddings.

It processes prepay, postpay, and HCDC claim data, builds embeddings from diagnosis/procedure descriptions, joins claim-level, provider, and agreement-level data, and applies Random Forest to predict erroneous claims.

---

## 📊 Key Highlights

- SQL Server data extraction using `pyodbc`
- Text embeddings from diagnosis/procedure using Azure OpenAI
- Agreement enrichment from provider contract data
- Embedding-based feature vectors from claim narrative
- RandomForest classification model with GridSearch
- AUC optimization and decile-level evaluation
- Automated email reporting using SMTP

---

## 🔁 Data Flow Diagram (Interactive)

```mermaid
graph TD
  A[SQL Data Load] --> B[Prepay / Postpay / HCDC Merge]
  B --> C[Diagnosis & Procedure Text Enrichment]
  C --> D[Agreement & Provider Info Join]
  D --> E[Azure OpenAI Embedding Generation]
  E --> F[Feature Engineering]
  F --> G[Random Forest Classifier]
  G --> H[Model Evaluation (AUC, Deciles)]
  H --> I[Email Reporting]
