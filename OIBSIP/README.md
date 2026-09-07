# Oasis Infobyte SIP — Data Analytics Internship Portfolio

![Internship](https://img.shields.io/badge/Oasis%20Infobyte-SIP%20Data%20Analytics-0052CC?style=for-the-badge&logo=google-analytics&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.13%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.7.2-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.2%2B-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Status](https://img.shields.io/badge/All%20Tasks-Completed%20(4%2F4)-success?style=for-the-badge)

Welcome to the **Oasis Infobyte Internship Program (OIBSIP)** Data Analytics repository. This portfolio houses all four end-to-end industry-grade data analytics, machine learning, and data engineering projects completed during the internship tenure.

Each task includes an **executed, interactive Jupyter Notebook**, **comprehensive technical documentation (`README.md`)**, **clean datasets**, and **high-resolution visualization artifacts (300 DPI)**.

---

## 📑 Portfolio Index & Overview

| Task | Project Title | Primary Objective | Tech Stack | Notebook Link | Documentation |
| :---: | :--- | :--- | :--- | :---: | :---: |
| **01** | **[Retail Sales EDA](Data-Analytics-Level1-Task1-Retail-Sales-EDA/)** | Uncover revenue drivers, seasonality, demographic buying patterns, and pricing elasticity. | Python, Pandas, Matplotlib, Seaborn | [View Notebook](Data-Analytics-Level1-Task1-Retail-Sales-EDA/OIBSIP_Task1_Retail_EDA.ipynb) | [Task 1 README](Data-Analytics-Level1-Task1-Retail-Sales-EDA/README.md) |
| **02** | **[Customer Segmentation](Data-Analytics-Level1-Task2-Customer-Segmentation/)** | RFM feature engineering, CLV modeling, and unsupervised K-Means clustering ($K=4$). | Scikit-Learn, Pandas, NumPy, Seaborn | [View Notebook](Data-Analytics-Level1-Task2-Customer-Segmentation/OIBSIP_Task2_Customer_Segmentation.ipynb) | [Task 2 README](Data-Analytics-Level1-Task2-Customer-Segmentation/README.md) |
| **03** | **[Data Cleaning & Hygiene Pipeline](Data-Analytics-Level1-Task3-Cleaning-Data/)** | Audit, clean, standardize, and validate messy enterprise data with strict business rules. | Pandas, NumPy, Scikit-Learn, OpenPyXL | [View Notebook](Data-Analytics-Level1-Task3-Cleaning-Data/OIBSIP_Task3_Cleaning_Data.ipynb) | [Task 3 README](Data-Analytics-Level1-Task3-Cleaning-Data/README.md) |
| **04** | **[Sentiment Analysis & NLP](DataAnalytics-Level1-Task4-Sentiment-Analysis/)** | 3-Class text sentiment classification comparing MNB vs. Logistic Regression (+18.1% Macro F1). | NLTK, Scikit-Learn, WordCloud, Pandas | [View Notebook](DataAnalytics-Level1-Task4-Sentiment-Analysis/OIBSIP_Task4_Sentiment_Analysis.ipynb) | [Task 4 README](DataAnalytics-Level1-Task4-Sentiment-Analysis/README.md) |

---

## 🎯 Task Summaries & Key Deliverables

### 🔹 Task 1: Exploratory Data Analysis (EDA) on Retail Sales
- **Objective:** Analyze retail transaction patterns across product categories, global territories, and customer demographics to inform merchandising and pricing strategies.
- **Key Methodologies:** Descriptive statistical profiling, monthly/quarterly time-series aggregation, demographic cohort segmentation, Pearson correlation matrices, and discount-to-profit margin elasticity modeling.
- **Primary Findings:**
  - **Revenue Leadership:** Electronics drove 35.8% of total gross sales ($52,786), with Laptops and Smartphones demonstrating the highest gross margins (83.1%).
  - **Seasonal Trajectory:** Q2 experienced an 11.8% expansion over Q1, peaking in March ($27,082).
  - **Demographic Signal:** The 26–35 millennial cohort commanded the highest Average Order Value ($784.15).
- 📁 **Folder:** [`Data-Analytics-Level1-Task1-Retail-Sales-EDA/`](Data-Analytics-Level1-Task1-Retail-Sales-EDA/)

---

### 🔹 Task 2: Customer Segmentation Analysis (RFM & K-Means)
- **Objective:** Construct behavioral customer segments to replace generic mass marketing with targeted, personalized lifecycle campaigns.
- **Key Methodologies:** Recency, Frequency, Monetary (RFM) feature engineering, historical Customer Lifetime Value (CLV) proxy calculation, log transformations, `StandardScaler` normalization, Elbow Method ($WSS$) and Silhouette Score ($K=4$, score = 0.442).
- **Segment Breakdown:**
  1. **Champions (18.2%):** Recency: 14 days, Frequency: 12.8 orders, Monetary: $5,240. *Action: VIP concierge, early access.*
  2. **Loyal Customers (31.4%):** Recency: 42 days, Frequency: 5.6 orders, Monetary: $1,820. *Action: Loyalty tiers, cross-selling.*
  3. **Potential Loyalists (28.1%):** Recency: 68 days, Frequency: 2.1 orders, Monetary: $620. *Action: Category onboarding, nurturing.*
  4. **At-Risk / Inactive (22.3%):** Recency: 215 days, Frequency: 1.2 orders, Monetary: $280. *Action: Win-back discounts, exit surveys.*
- 📁 **Folder:** [`Data-Analytics-Level1-Task2-Customer-Segmentation/`](Data-Analytics-Level1-Task2-Customer-Segmentation/)

---

### 🔹 Task 3: Data Cleaning & Hygiene Pipeline
- **Objective:** Demonstrate rigorous data hygiene by transforming deliberately flawed, noisy retail transaction records into an audit-ready dataset (`cleaned_retail_data.csv`).
- **Key Methodologies:** Missing-value diagnosis, full-row duplicate elimination, mixed timestamp normalization (`datetime64[ns]`), string standardization and dictionary lookups, IQR-based outlier analysis, and transactional integrity validation (`Total_Sales == Quantity * Unit_Price * (1 - Discount_Rate)`).
- **Pipeline Results:**
  - **100% Completeness:** Successfully resolved nulls across 8 feature fields without introducing statistical bias.
  - **Deduplication:** Purged 35 redundant logging records.
  - **Integrity Validation:** Repaired 28 pricing discrepancies and pruned impossible demographic entries.
- 📁 **Folder:** [`Data-Analytics-Level1-Task3-Cleaning-Data/`](Data-Analytics-Level1-Task3-Cleaning-Data/)

---

### 🔹 Task 4: Sentiment Analysis Pipeline & ML Benchmark
- **Objective:** Classify unstructured customer sentiment into Positive, Neutral, and Negative classes to automate customer support triage and monitor brand reputation.
- **Key Methodologies:** HTML/URL/Mention regex cleaning, negation-preserving stopword tokenization, WordNet lemmatization, sublinear TF-IDF vectorization (1-2 n-grams, 5,000 features), 80/20 stratified split, and model benchmarking between Multinomial Naive Bayes and Logistic Regression.
- **Benchmark Results:**
  - **Logistic Regression (Champion):** **77.96% Accuracy** | **0.6937 Macro F1** (vs. MNB's 0.5872 Macro F1) — an **18.1% relative improvement** in balanced performance.
  - **WordCloud Visualizations:** Extracted distinct lexical signatures for praise, operational questions, and service grievances.
  - **Error Analysis:** Conducted root-cause investigations on 5 misclassified test samples (sarcasm, mixed polarity, domain vocabulary bias).
- 📁 **Folder:** [`DataAnalytics-Level1-Task4-Sentiment-Analysis/`](DataAnalytics-Level1-Task4-Sentiment-Analysis/)

---

## 🛠️ Global Tech Stack & Dependencies

```text
Language:            Python 3.13+
Core Data Libs:      Pandas (2.2+), NumPy (2.0+)
Machine Learning:    Scikit-Learn (1.7+)
NLP & Text:          NLTK (3.9+), WordCloud (1.9+)
Visualizations:      Matplotlib (3.11+), Seaborn (0.13+)
Environment:         Jupyter Notebook / JupyterLab
```

To install all dependencies across the entire repository:

```bash
pip install pandas numpy scikit-learn nltk matplotlib seaborn wordcloud openpyxl jupyter
```

---

## 👤 Author & Acknowledgments

- **Intern:** Subrahmanyeswara Yedula
- **Program:** Oasis Infobyte Internship Program (OIBSIP)
- **Track:** Data Analytics (Level 1)
- **GitHub:** [@subbu212005](https://github.com/subbu212005)
