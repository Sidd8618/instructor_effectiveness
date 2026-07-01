# Instructor Effectiveness Analysis

Exploratory data analysis and predictive modeling on a 2,000-row instructor/course engagement dataset, built as a data science internship assignment for Accredian.

## Objective
Understand what drives course completion, and build a model that predicts `completion_rate` from student engagement and performance signals.

## Contents
- `instructor_effectiveness_analysis.ipynb` — full analysis notebook
- `instructor_effectiveness_dataset_2000_rows.csv` — dataset (2,000 rows, 12 columns, no missing values or duplicates)

## Approach
1. Data cleaning & sanity checks
2. Exploratory data analysis — distributions, correlations, course-level comparisons
3. Statistical testing — Welch's t-test comparing completion rates by forum engagement
4. Feature engineering — a custom 0–100 Instructor Effectiveness Score
5. Predictive modeling — Linear Regression vs. Random Forest for `completion_rate`
6. Instructor-level aggregation and ranking

## Key Findings
- **`avg_score_improvement`** is the strongest driver of completion rate — both the highest correlation (r ≈ 0.40) and the top Random Forest feature importance (~31%), ahead of quiz scores and feedback.
- Courses with **above-median forum activity** have significantly higher mean completion rates (t ≈ 6.29, p ≈ 4.0e-10).
- **Linear Regression (R² ≈ 0.33)** slightly outperformed Random Forest (R² ≈ 0.28) on held-out data, suggesting the relationships are largely linear.
- The model explains roughly a third of the variance in completion rate — engagement/performance features are meaningful but not the whole story (course difficulty, student background, etc. aren't captured here).

## Details
Data Science Internship Assignment, Accredian
