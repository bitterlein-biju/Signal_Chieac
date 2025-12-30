# Signal_Chieac
CHIEAC PROJECT 
![]("signal/SweatSignal.jpg")

# SweatSignal – Wellness Impact Analytics Platform

SweatSignal is a privacy-first data platform that enables wellness practitioners to collect anonymous emotional feedback, analyze client impact using machine learning, and publish transparent public reports.

---

## Features
- QR-based feedback collection  
- Practitioner profile creation  
- Azure-powered ingestion pipeline  
- Databricks data processing  
- ML-driven sentiment analysis  
- Public practitioner impact pages  
- Automated PDF impact reports  

---

## Tech Stack  
- Azure Blob Storage  
- Azure Databricks (PySpark)  
- Azure SQL Database  
- Flask (Python Web App)  
- Scikit-learn (TF-IDF + Logistic Regression)  
- ReportLab & Matplotlib  

---

## Architecture
Client → QR Code → Flask App → Azure Blob → Azure Data Factory → Azure Databricks → Azure SQL → Public Pages & PDF Reports  

Secrets and credentials are securely managed using **Azure Key Vault**.

---

## How It Works
1. Practitioner creates a profile using the web app  
2. A QR code is generated for that practitioner  
3. Clients scan the QR and submit anonymous feedback  
4. Feedback is stored in Azure Blob Storage  
5. Azure Data Factory triggers Databricks  
6. Databricks cleans data and applies ML sentiment scoring  
7. Results are stored in Azure SQL  
8. Public dashboards and PDF reports are automatically generated  

---

## Machine Learning
Client comments are classified into three categories:
- Positive  
- Neutral  
- Constructive / Negative  

A TF-IDF vectorizer with Logistic Regression is used to train and score feedback.  
These scores power trend charts, practitioner rankings, and public impact pages.

---

## Data Model
The platform uses a star schema:

**Dimensions**
- Practitioner  
- Session  
- Survey Question  

**Fact Table**
- Client Feedback  

This enables fast analytics for emotional change, sentiment, and practitioner performance.

---

## Impact Reporting
Each practitioner can generate a PDF report containing:
- Average emotional change  
- Positive experience percentage  
- Weekly emotional trendline  
- Sentiment breakdown  
- Top client themes  
- Audit timestamp  

File format:
```
SweatSignal_ImpactReport_<PractitionerID>.pdf
```

---

## Why This Matters
Wellness professionals often rely on subjective feedback.  
SweatSignal provides **data-driven, ethical, and transparent impact measurement** for:
- Studios  
- Trainers  
- Therapists  
- Grant applications  
- Community accountability  

---

## Built By
**Bitterlein Konnoth Biju**  
Azure Data Engineer | Analytics Engineer | ML-Enabled Data Platforms  
