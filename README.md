# Card (1995) IV Replication

## Track Chosen:
Labor Economics / Causal Inference Track

## Paper:
Card, David (1995). "Using Geographic Variation in College Proximity to Estimate the Return to Schooling."

## Research Question:
Does additional schooling causally increase wages? 
The paper uses proximity to a four-year college as an instrumental variable to estimate the causal return to education, addressing potential ability bias in OLS estimates.
# Estimating the Return to Schooling: Replication and Extension of Card (1995)

## Overview
This project replicates and extends Card (1995), which investigates the causal effect of education on wages using geographic variation in college proximity as an instrumental variable.

The main research question is:
**What is the causal return to schooling, and does it differ across individuals?**

---

## Methodology

### Phase 1: Data Preparation
- Parsed raw `.dat` and `.sas` files
- Converted data into a structured pandas DataFrame
- Cleaned missing values and constructed variables (e.g., age squared)

### Phase 2: Baseline Analysis
- Estimated OLS regression of wages on education
- Implemented Instrumental Variables (IV / 2SLS) using proximity to college (`nearc4`)
- Compared OLS and IV estimates to address endogeneity

### Phase 3: Extension – Heterogeneous Treatment Effects (HTE)
- Allowed returns to schooling to vary across demographic groups
- Interacted schooling with:
  - Race (`black`)
  - Region (`south66`)
- Instrumented both education and interaction terms using:
  - `nearc4`
  - `nearc4 × demographic`

---

## Key Findings

- IV estimates of the return to schooling are **higher than OLS**, suggesting OLS underestimates the causal effect.
- Returns to schooling are **not uniform across individuals**.
- Evidence suggests that demographic factors (race and region) influence the magnitude of education returns.

---

## Data

- Source: National Longitudinal Survey (NLS)
- Raw data: `/data/raw`
- Processed data: `/data/processed`

---

## Repository Structure
