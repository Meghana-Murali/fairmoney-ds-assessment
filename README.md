# FairMoney Senior Data Scientist Assessment

**Submitted by:** Meghana Murali  
**Date:** August 5th, 2025

---

### Project Overview

This repository contains the solution for the Senior Data Scientist take-home assessment from FairMoney. The assignment 
was divided into two independent tasks:

1.  **Feature Engineering:** To process semi-structured JSON credit report data and create a reusable function that extracts a rich set of predictive features.
2.  **Predictive Modeling:** To use a historical loan dataset (`credit.csv`) to train, validate, and interpret a machine learning model to predict loan default.

The goal was not only to build a high-performing model but also to demonstrate a professional, end-to-end data science workflow, from data analysis and critical thinking to clear communication of business impact.

---

### Repository Structure

```
/fairmoney-ds-assessment
│
├── 📂 data/
│ ├── credit.csv
│ └── credit_report_sample.json
│
├── 📂 images/
│ ├── credit_history_vs_default.png
│ └── ... (other saved plots)
│
├── 📂 notebooks/
│ ├── 📜 1_Feature_Engineering.ipynb
│ └── 📜 2_Modeling.ipynb
│
├── 📂 presentation/
│ └── 📄 Presentation_Meghana_Murali.pdf
│
├── 📜 .gitignore
├── 📜 README.md
└── 📜 requirements.txt
```

---

### How to Run This Project

To reproduce the analysis, please follow these steps:

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/Meghana-Murali/fairmoney-ds-assessment.git
    cd fairmoney-ds-assessment
    ```

2.  **Create a Virtual Environment:**
    ```bash
    python -m venv .venv
    ```
    
3. **Activate the Virtual Environment:**
    ```bash
    # On Windows: 
    .\.venv\Scripts\activate
    # On Mac/Linux: 
    source .venv/bin/activate
    ```
   
4. **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

5.  **Launch Jupyter and Run Notebooks:**
    ```bash
    jupyter lab
    ```
    Navigate to the `notebooks/` directory and run the notebooks in order.

---

### Summary of Key Findings & Recommendations

#### **Part 1: Feature Engineering**
*   Successfully engineered **58 features** from the raw JSON credit reports, covering categories like repayment history, delinquencies, credit-seeking behavior, and applicant stability.
*   The entire process was encapsulated into a single, reusable Python function.

#### **Part 2: Predictive Modeling**
*   Developed a tuned **XGBoost model** with a final **ROC AUC of 0.7845** on the test set.
*   **Key Insight:** Uncovered a highly counterintuitive pattern in the `credit_history` feature, flagging it as a potential data definition issue that requires business consultation.
*   **Ethical Consideration:** Explicitly excluded the `Gender` feature from the model to ensure a fair and responsible lending process.

#### **Final Business Recommendation**
The final model is a powerful tool for risk assessment. I recommend deploying it not as a simple approve/reject system, but as the foundation for a **strategic, risk-based lending policy**. By categorizing applicants into risk buckets (low, medium, high, very-high), FairMoney can optimize loan terms (e.g., adjust interest rates or loan amounts), thereby **maximizing approvals and revenue while mitigating credit losses.**


 
