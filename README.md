Fintech Review Analytics

Project Overview

This project delivers a complete data analytics workflow developed for Omega Consultancy. It focuses on analyzing customer reviews collected from the Google Play Store for three leading Ethiopian banks: Commercial Bank of Ethiopia (CBE), Bank of Abyssinia (BOA), and Dashen Bank.

Business Objective

As mobile banking continues to grow rapidly in Ethiopia, customer feedback has become a valuable source of insight into service quality and user experience. When properly analyzed, these reviews provide actionable intelligence that helps banking product teams improve customer satisfaction, retention, and application performance.

Key Business Use Cases

Customer Retention: Identifying recurring technical problems such as app crashes, slow performance, or failed transactions across banking applications.
Feature Improvement: Discovering customer-requested features like biometric authentication or personal finance tools to support future development.
Complaint Analysis: Grouping repeated complaints such as login failures or missing OTP codes to improve customer support prioritization.

Project Structure
fintech-review-analytics/
├── .github/workflows/        # GitHub Actions for CI/CD
├── data/
│   ├── raw/                  # Raw scraped review datasets
│   ├── plots/                # Visualization outputs
│   └── analyzed_reviews.csv  # Processed review dataset
├── notebooks/                # Exploratory analysis notebooks
│   └── task4_insights.ipynb  # Visual analytics notebook
├── scripts/                  # Helper and utility scripts
├── src/                      # Main application source code
│   ├── scraper.py                # Review data collection
│   ├── preprocessing.py          # Data cleaning and preparation
│   ├── sentiment_analysis.py     # Sentiment analysis pipeline
│   ├── thematic_analysis.py      # Theme extraction and clustering
├── tests/                    # Unit and validation tests
├── requirements.txt          # Project dependencies
├── final_report.md           # Final analytical business report
└── README.md

Setup and Execution

1. Environment Configuration
# clone and Install required packages
pip install -r requirements.txt
python -m spacy download en_core_web_sm
2. Running the Data Pipeline

Run the following scripts sequentially:

# Data collection and preprocessing
python src/scraper.py
python src/preprocessing.py

# Sentiment and thematic analysis
python src/sentiment_analysis.py
python src/thematic_analysis.py
3. Database Management (Task 3)
python src/database_manager.py
4. Visualization and Reporting (Task 4)

Open notebooks/task4_insights.ipynb using a Jupyter-supported environment such as VS Code or Jupyter Notebook to generate visualizations and analytical insights. Final findings are summarized in final_report.md.

5. Running Validation Tests

# Execute pipeline validation tests
python -m unittest tests/test_pipeline.py
Project Progress
Task 1: Successfully collected and preprocessed 1,500 reviews while maintaining full data consistency.
Task 2: Completed sentiment and thematic analysis with automated visualization support.
Task 3: Designed a PostgreSQL relational database schema (scripts/schema.sql) and implemented automated data insertion using psycopg2. Verification queries were also developed in scripts/verify_data.sql.
Task 4: Developed advanced analytical visualizations in notebooks/task4_insights.ipynb.
Technologies and Tools
Database: PostgreSQL, psycopg2
Natural Language Processing: transformers (DistilBERT), spaCy
Data Analysis: pandas, scikit-learn
Visualization: matplotlib, seaborn
CI/CD: GitHub Actions