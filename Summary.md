# Project Context & Master Execution Plan
**Course:** AIMLCZG549 - API-driven Cloud Native Solutions (Assignment I)  
**Project Name:** Real-Time Insurance Claims Anomaly Detection Pipeline  
**Weight:** 15 Marks | **Format:** Group Project (2-4 Members) | **Deadline:** August 18

## 1. Business Problem & Architecture Strategy
We are building a cloud-native DataOps pipeline to identify anomalous or potentially fraudulent vehicle insurance claims in near real-time. Instead of treating the Kaggle "Auto Insurance Claims Data" as a static file, we will simulate a continuous data stream. A scheduled orchestrator will fetch new batches of claims every 2 minutes, process them, and update analytics dynamically. 

This architecture perfectly fulfills the assignment requirements by combining standard Machine Learning EDA with modern Cloud Data Engineering (DataOps).

## 2. Technology Stack & Tools
* **Workspace & Version Control:** Google Colab (compute) integrated with GitHub (code persistence & collaboration).
* **Data Processing & ML:** Python (`pandas` for cleaning, `scikit-learn` for normalization/encoding, `matplotlib`/`seaborn` for visualization).
* **DataOps & Orchestration:** **Prefect Cloud**. This provides the `@flow` and `@task` framework to schedule the Python scripts to run every 2 minutes and provides the mandatory "Cloud Dashboard" for monitoring.
* **API Testing:** Postman (or Python `requests`) to query Prefect's REST APIs.

---

## 3. Rubric Mapping & Action Plan

### Phase 1: Data Pipeline Design & Development (10 Marks)
* **[1.1] Business Understanding:** Defined above (Insurance fraud detection).
* **[1.2] Data Ingestion:** Download Kaggle dataset (`insurance_claims.csv`). Simulate live ingestion by reading data batches.
* **[1.3] Data Pre-processing:** 
  * Generate summary statistics (`df.describe()`).
  * Check and impute missing values (e.g., median for numeric, mode for categorical).
  * Validate data types (`df.info()`).
  * Normalize/scale numerical features (e.g., Min-Max scaling on `claim_amount`).
* **[1.4] Exploratory Data Analysis (EDA):**
  * Encode categorical text to numbers (e.g., One-Hot Encoding for `vehicle_type`).
  * Perform binning (e.g., converting continuous `age` into `age_groups`).
  * Calculate correlation coefficients (Correlation Matrix).
  * Plot feature importance.
  * Generate univariate (histograms) and bivariate (scatter plots) charts.
* **[1.5] DataOps:** Refactor Phase 1.3 and 1.4 into Python functions. Wrap them in Prefect decorators, deploy to Prefect Cloud, and schedule via cron `*/2 * * * *`. Log all outputs.

### Phase 2: API Access (5 Marks)
* **[3.1 & 3.2] Retrieve & Display Details:** Use Prefect Cloud's REST API to fetch at least 4 application details (e.g., Flow ID, Deployment configurations, Run statuses, Work pool availability).
* **[3.3] API Documentation:** Execute tests in Postman, verify `200 OK` HTTP status codes, and capture screenshots of requests/responses.

### Phase 3: Final Deliverables
* **Word Document:** Screenshots of the Colab output, Prefect Cloud dashboard, and Postman API responses, plus explanations. Explicitly highlight individual member contributions.
* **Video Demonstration:** A recorded walkthrough of the code, cloud dashboard, and API responses, uploaded to a shared Google Drive.

---

## 4. Current Progress & Next Steps
**What is completed:**
1. GitHub repository initialized with `README.md` and `PROGRESS.md`.
2. Google Colab workspace created, JSON syntax error resolved, and successfully linked to the GitHub repository.

**Immediate Next Action for the Group:**
Upload the raw Kaggle dataset into the active Colab session and execute the initial ingestion script to profile the data:
```python
import pandas as pd

# Load dataset
df = pd.read_csv('/content/insurance_claims.csv')

# Profile the data
print(f"Shape: {df.shape}\n")
display(df.head())
df.info()
