---

### `PROGRESS.md`

```markdown
# Assignment Progress Tracker

Use this file to track our group's progress against the official AIMLCZG549 rubric. Mark tasks with an `x` when completed: `- [x]`

## Phase 1: Pipeline & Analytics (Weight: 10 Marks)

- [ ] **1.1 Business Understanding**
  - [ ] Define the business problem (Insurance claims anomaly/fraud detection).
- [ ] **1.2 Data Ingestion**
  - [ ] Download the Auto Insurance Claims dataset from Kaggle.
  - [ ] Write Python script/Colab cell to load and sample records.
- [ ] **1.3 Data Pre-processing**
  - [ ] Display summary statistics (`df.describe()`).
  - [ ] Check for and impute missing values for numeric columns.
  - [ ] Verify and correct data types (`df.info()`).
  - [ ] Normalize/scale numeric data.
- [ ] **1.4 Exploratory Data Analysis (EDA)**
  - [ ] Calculate correlation coefficients (Correlation Matrix).
  - [ ] Perform binning on appropriate features (e.g., claimant age).
  - [ ] Encode categorical features (e.g., policy state, vehicle type).
  - [ ] Assess and plot feature importance.
  - [ ] Generate visualizations (Univariate and Bivariate charts).
- [ ] **1.5 DataOps Automation**
  - [ ] Wrap ingestion, pre-processing, and EDA logic into functions.
  - [ ] Decorate functions with Prefect `@task` and `@flow`.
  - [ ] Deploy flow to Prefect Cloud.
  - [ ] Schedule workflow to run every 2 minutes.
  - [ ] Verify execution logs and status on the Prefect Cloud dashboard.

## Phase 2: API Integration (Weight: 5 Marks)

- [ ] **3.1 Retrieve Application Details**
  - [ ] Use built-in APIs (Prefect REST API) to access pipeline metadata.
- [ ] **3.2 Display Application Details**
  - [ ] Extract and present at least 4 details (e.g., Flow ID, Deployment Schedule, Run Status, Work Pool Status).
- [ ] **3.3 API Testing & Documentation**
  - [ ] Test the APIs using Postman or an API client.
  - [ ] Verify HTTP status codes (e.g., 200 OK).
  - [ ] Capture screenshots of request/response bodies.

## Phase 3: Final Deliverables

- [ ] **Documentation**
  - [ ] Compile Word document with project details and explanations.
  - [ ] Insert application and API screenshots.
  - [ ] Clearly highlight the contribution of each group member.
- [ ] **Video Demonstration**
  - [ ] Record a video demonstrating the entire pipeline and API retrieval.
  - [ ] Upload video to shared Google Drive.
- [ ] **Submission**
  - [ ] One group member uploads the Word document to the portal.
  - [ ] Ensure Google Drive video link is accessible.
