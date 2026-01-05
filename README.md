# End-to-End A/B Testing & Experiment Analysis

## Project Overview
This project demonstrates an end-to-end workflow for A/B testing and experiment analysis. It includes data processing, statistical tests, sample size validation, metric calculation, and visualization. The project uses a publicly available website conversion dataset from [Kaggle](https://www.kaggle.com/) (ab_data.csv).

**Goal:** Evaluate the impact of an A/B experiment on user conversion and revenue, ensuring statistical validity and providing actionable insights.

---

## Project Steps

1. **Data Loading and Cleaning**
   - Load the `ab_data.csv` dataset
   - Inspect data for missing values and inconsistencies
   - Simulate a `revenue` column for analysis purposes

2. **Metric Calculation**
   - Compute key metrics per group:
     - Users
     - Conversions
     - Conversion Rate
     - Revenue per User

3. **Statistical Testing**
   - Chi-square test for conversion differences
   - T-test for revenue differences
   - Interpret p-values for statistical significance

4. **Sample Size Efficiency Check**
   - Validate whether the sample size is sufficient to detect a minimum detectable lift
   - Perform power analysis using `statsmodels`
   - Compare required sample size vs actual group sizes

5. **Visualization & Dashboard**
   - Prepare daily metrics for visualization
   - Build a Tableau dashboard (optional screenshot included) showing:
     - KPI summary
     - Conversion and revenue by group
     - Trend over time
     - Sample size sufficiency
     - Insights / recommendations

---

## Dataset
- Original dataset: `ab_data.csv`  
  - Columns: `user_id`, `timestamp`, `group` (control/treatment), `landing_page`, `converted`
- Revenue column is simulated for analysis

---

## Code
- All Python code is included in [`code/ab_testing_analysis.ipynb`](code/ab_testing_analysis.ipynb)
- Libraries used:
  - Python (Pandas, NumPy, SciPy, statsmodels)
  - Tableau (dashboard visualization)

---

## Dashboard Screenshot
[Dashboard Screenshot](dashboard/ab_testing_screenshot.png)

---

## Key Insights
- Conversion difference between treatment and control: Statistically not significant  
- Revenue difference: Slightly negative / Statistically not significant  
- Sample size sufficient to detect desired lift: ✅  
- Recommendation: Decline treatment roll out

---

## Skills Demonstrated
- Data extraction, cleaning, and manipulation (Python, SQL)
- Statistical testing (Chi-square, T-test)
- Experiment validation & sample size analysis
- Dashboard creation (Tableau)
- Communication of actionable business insights

---

## How to Run
1. Clone the repository
2. Open `code/ab_testing_analysis.ipynb` in Jupyter Notebook
3. Install required libraries if necessary:
```bash
pip install pandas numpy scipy statsmodels
````
4. Run the notebook step by step to reproduce all metrics and analysis
