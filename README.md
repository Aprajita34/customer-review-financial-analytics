# customer-review-financial-analytics
A Python tool that analyses customer reviews to calculate lost revenue risk and recommend product fixes.
# Customer Review & Financial Analytics Assistant

An end-to-end Python analytics pipeline hosted in Google Colab that ingests unstructured customer reviews, performs NLP sentiment analysis, quantifies Annual Recurring Revenue (ARR) churn risk, and extracts domain-specific product pain points using machine learning.

## Key Features

* **Financial Risk Quantification:** Links customer review ratings to customer subscription metrics to calculate total Monthly and Annual Revenue at Risk (ARR).
* **NLP Sentiment Scoring:** Utilizes `TextBlob` pattern-based sentiment scoring to isolate negative customer feedback.
* **Domain-Specific Keyword Extraction:** Implements `scikit-learn` TF-IDF vectorization to extract top product pain points without manual text reading.
* **Multi-Domain Adaptability:** Designed as a modular function capable of ingesting and analyzing CSV files across different product categories (e.g., Tech Hardware, E-Commerce Retail, Fintech).

## Tech Stack

* **Environment:** Google Colab
* **Language:** Python 3
* **Data Manipulation:** Pandas, NumPy
* **Machine Learning & NLP:** scikit-learn (TF-IDF Vectorizer), TextBlob

## How to Run

1. Open `Customer_Review_and_Financial_Analytics_Assistant.ipynb` in Google Colab.
2. Execute the notebook cells sequentially.
3. Upload any customer review dataset containing `Rating` and `Review Text` columns when prompted.

## Sample Pipeline Output
```text
==========================================================
     FINANCIAL & PRODUCT STRATEGY REPORT: AMAZON_REVIEWS.CSV
==========================================================
Total Reviews Processed   : 300
At-Risk Customers         : 84
Projected Churn Risk Rate : 28.0%
Annual Revenue at Risk    : $115,200.00
----------------------------------------------------------
NEW EXTRACTED PAIN POINTS (AUTOMATICALLY ADAPTED):
  1. BATTERY
  2. CHARGING
  3. SCREEN
  4. SUPPORT
----------------------------------------------------------
AUTOMATED PRD & ACTION PLAN:
• Core Priority Area : Resolve critical 'BATTERY' and 'CHARGING' issues.
• Capital at Risk    : $115,200.00 ARR.
• Recommended Action : Allocate engineering resources to fix battery optimization.
==========================================================
```
