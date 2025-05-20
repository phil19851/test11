# Smart Audit Claim Processing with AI Enrichment

This project automates the process of claim audit analysis using Python and AI services from Azure OpenAI. It extracts, transforms, and enriches claim data to build predictive models for identifying erroneous claims.

## 📌 Key Features

- ✅ Claim extraction from SQL Server using `pyodbc`
- ✅ Prepay, postpay, and HCDC claim data merging
- ✅ Feature engineering with claim, provider, and line-level enrichment
- ✅ Agreement-level data joining
- ✅ Textual embedding using Azure OpenAI embeddings
- ✅ Classification using `RandomForestClassifier`
- ✅ Performance evaluation including AUC, decile, and precision-recall analysis
- ✅ Auto-email reporting using SMTP
- ✅ Data exported for dashboard/reporting

## 🔧 Technologies Used

- Python (Pandas, Scikit-learn, XGBoost)
- Azure OpenAI for embeddings
- SQL Server (via `pyodbc`)
- Email automation via `smtplib`
- Data exported to Excel for dashboards

## 🗂️ Project Structure

- `Prepay`, `Postpay`, `HCDC` Claim Data Load
- Claim Enrichment:
  - Diagnosis & Procedure Embeddings
  - Provider Agreement Details
  - Line-level Metrics
- Model Training and Evaluation
- ROC Curve, Feature Importance, and Top-N Error Identification
- Email Reporting with AUC scores

## 📤 Output

- `train_Df.xlsx`, `dep.xlsx`: Training data
- `Top_Feature_Importances.xlsx`: Feature ranking
- `Decile_Table_RF1.xlsx`: Decile analysis
- `random_forest_error_cat_best.pkl`: Trained model
- `Claim_Details` & `Agreement_desc`: Human-readable audit summaries

## 🚀 How to Run

1. Configure database connection (`pyodbc` and server details)
2. Provide Azure OpenAI key and endpoint
3. Run the notebook or script from start to finish
4. Review outputs saved as Excel and pickle files
5. Review results via auto-generated email or logs

## 🔐 Security & Access

Ensure:
- SQL Server access credentials are protected.
- Azure API keys are not hardcoded in shared environments.

---

_This project is intended for use within TMG Smart Audit team (JHH, MAPD, MMAI lines of business)._
