# Fintech Review Analytics

## Project Overview
This project delivers a complete data analytics workflow developed for Omega Consultancy. It focuses on analyzing customer reviews collected from the Google Play Store for three leading Ethiopian banks: Commercial Bank of Ethiopia (CBE), Bank of Abyssinia (BOA), and Dashen Bank.

### Business Objective


As mobile banking continues to grow rapidly in Ethiopia, customer feedback has become a valuable source of insight into service quality and user experience. When properly analyzed, these reviews provide actionable intelligence that helps banking product teams improve customer satisfaction, retention, and application performance.

### Business Scenarios
1.  **Retaining Users:** Analyzing systemic issues like slow loading or transfer failures across all three apps.
2.  **Enhancing Features:** Extracting desired features (e.g., fingerprint login, budgeting tools) to guide development.
3.  **Managing Complaints:** Clustering recurring complaints (e.g., "login error", "OTP not received") to guide customer support prioritization.

---

## Project Structure
```text
fintech-review-analytics/
├── .github/workflows/    # CI/CD (GitHub Actions)
├── data/
│   ├── raw/             # Raw scraped CSV data
│   ├── plots/           # Generated visualizations
│   └── analyzed_reviews.csv # Final processed data
├── notebooks/           # Research and EDA notebooks
│   └── task4_insights.ipynb  # Task 4: Visualizations
├── scripts/             # Utility scripts
├── src/                 # Core source code
│   ├── scraper.py           # Task 1: Data collection
│   ├── preprocessing.py     # Task 1: Data cleaning
│   ├── sentiment_analysis.py # Task 2: Sentiment scoring
│   ├── thematic_analysis.py  # Task 2: Theme extraction
├── tests/               # Unit and sanity tests
├── requirements.txt      # Dependencies
├── final_report.md       # Task 4: Final Business Report
└── README.md
```

---

## How to Run

### 1. Environment Setup
```bash
# Clone the repository
git clone https://github.com/Furtunaa/Fintech-Review-Analytics-week2.git

# Install dependencies
pip install -r requirements.txt
python -m spacy download en_core_web_sm
```

### 2. Data Pipeline
Execute the scripts in the following order:
```bash
# Task 1: Collect and Preprocess data
python src/scraper.py
python src/preprocessing.py

# Task 2: Analyze Sentiment and Themes
python src/sentiment_analysis.py
python src/thematic_analysis.py
```

### 3. Database Integration (Task 3)
```bash
python src/database_manager.py
```

### 4. Visualizations & Reporting (Task 4)
Open `notebooks/task4_insights.ipynb` in your preferred Jupyter environment (e.g., VS Code) to generate the final plots. The final business insights are documented in `final_report.md`.

### 5. Running Tests
```bash
# Run sanity tests to verify environment and data
python -m unittest tests/test_pipeline.py
```

---

## Progress Summary
*   **Task 1:** 1,500 reviews collected and preprocessed with 100% data integrity.
*   **Task 2:** Sentiment and Thematic analysis complete with automated visualizations.
*   **Task 3:** PostgreSQL relational schema designed (`scripts/schema.sql`). Automated Python script (`psycopg2`) written to insert and structure the cleaned data. SQL queries written to verify data integrity (`scripts/verify_data.sql`).
*   **Task 4:** Advanced visualizations implemented in Jupyter Notebook (`notebooks/task4_insights.ipynb`)

---

## Technologies Used
*   **Database:** PostgreSQL, `psycopg2`
*   **NLP:** `transformers` (DistilBERT), `spaCy`
*   **Analysis:** `pandas`, `scikit-learn`
*   **Visualization:** `matplotlib`, `seaborn`
*   **CI/CD:** GitHub Actions
