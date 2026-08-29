# Project: Real-Time Insurance Claims Anomaly Detection

### Group Members
* [Member 1 Name] - [Contribution/Role]
* [Member 2 Name] - [Contribution/Role]
* [Member 3 Name] - [Contribution/Role]
* [Member 4 Name] - [Contribution/Role]

### Project Overview
This project is a Cloud-based Data Science/Machine Learning application designed to simulate and process a real-time stream of vehicle insurance claims. The architecture includes an automated data pipeline for continuous ingestion, pre-processing, and exploratory data analysis (EDA), orchestrated using cloud-native DataOps practices.

### Tech Stack
* **Environment:** Google Colab / Local Python Virtual Environment
* **Data Processing & EDA:** Python (`pandas`, `scikit-learn`, `matplotlib`, `seaborn`)
* **Orchestration (DataOps):** Prefect Cloud (Workflows & Scheduling)
* **API Testing:** Postman / Python `requests`

### Objectives Addressed
1. **Design and Development of a Data Pipeline:**
   * **Ingestion:** Automated batch processing of a Kaggle insurance dataset.
   * **Pre-processing:** Missing value imputation, normalization, and data type formatting.
   * **EDA:** Correlation coefficients, feature importance, binning, and bivariate visualization.
   * **DataOps:** Pipeline automated to run every 2 minutes via Prefect Cloud with live dashboard monitoring.
2. **API Access:**
   * Extraction of application details (flows, deployments, runs, work pools) using REST APIs.

### Repository Structure
```text
├── data/
│   ├── raw/                 # Original Kaggle dataset (exclude from version control if large)
│   └── processed/           # Cleaned output data
├── notebooks/
│   └── pipeline.ipynb       # Main Google Colab notebook
├── src/
│   └── workflow.py          # Python scripts for Prefect tasks and flows
├── docs/
│   └── api_screenshots/     # Postman/API test evidence
├── PROGRESS.md              # Task tracking and assignment checklist
└── README.md
