# Hospital Readmission Risk Prediction System

**Reducing hospital penalties and improving patient care through predictive analytics**

## Project Overview

This project analyzes CMS (Centers for Medicare & Medicaid Services) hospital readmission data to predict which hospitals are at high risk for excessive readmissions. The goal is to identify actionable interventions that can reduce CMS penalties and improve patient care quality.

### Business Impact
- **$5.96 Billion** total financial exposure across analyzed hospitals
- **$1.46 Billion** potential savings with 25% readmission reduction
- **81.8%** of hospitals currently exceed expected readmission rates

## Problem Statement

The CMS Hospital Readmissions Reduction Program (HRRP) penalizes hospitals with readmission rates above expected levels (Excess Readmission Ratio > 1.0). These penalties can cost hospitals $500K-$1M annually, while each preventable readmission costs $15,000-$20,000. This project aims to:

1. Predict which hospitals will have high readmission rates
2. Identify key risk factors driving readmissions
3. Calculate financial impact and ROI of interventions
4. Provide data-driven recommendations for improvement

## Data Sources

- **CMS Hospital Readmissions Reduction Program (FY 2025)**: Hospital-level readmission rates by condition
- **CMS Hospital General Information**: Hospital characteristics, ratings, and location
- **Total Records**: 8,121 hospital-condition combinations after cleaning

## Key Findings

### 1. Hospital Quality Ratings Strongly Predict Readmissions
- **1-star hospitals**: 79.1% have high readmission risk
- **5-star hospitals**: 32.7% have high readmission risk
- Clear inverse relationship between quality ratings and readmission rates

### 2. Geographic Patterns Identified
Top states with highest readmission rates:
- Massachusetts (MA): 1.055 ratio, 73.6% high-risk
- New Jersey (NJ): 1.031 ratio, 67.7% high-risk
- Mississippi (MS): 1.029 ratio, 68.0% high-risk

### 3. All Six Tracked Conditions Show Similar Patterns
- Heart Attack (AMI)
- Heart Surgery (CABG)
- Heart Failure (HF)
- Hip/Knee Replacement
- Pneumonia (PN)
- COPD

## Methodology

### Data Processing
1. Loaded and merged CMS datasets
2. Handled missing values and data quality issues
3. Created binary target variable (High Risk = Excess Readmission Ratio > 1.0)
4. Engineered features including risk categories and discharge metrics

### Exploratory Data Analysis
- Analyzed readmission patterns by condition, hospital type, and geography
- Identified correlations between hospital characteristics and readmission rates
- Calculated financial impact of current readmission levels

### Machine Learning Models
Compared three classification algorithms:
- **Logistic Regression**: Baseline model
- **Random Forest**: Ensemble method
- **Gradient Boosting**: Best performer (selected)

### Model Performance
- **Accuracy**: 100%
- **ROC-AUC Score**: 1.000
- **Precision/Recall**: 1.00 for both classes

### Top Predictive Features
1. Readmission Gap (Predicted - Expected Rate)
2. Expected Readmission Rate
3. Predicted Readmission Rate
4. Number of Discharges
5. Hospital Star Rating

## Business Recommendations

### 1. Implement Risk Stratification System
Deploy predictive model to identify high-risk hospitals in real-time for targeted interventions

### 2. Prioritize Low-Rated Hospitals
Focus quality improvement programs on 1-2 star hospitals (79% high-risk rate)

### 3. Geographic Resource Allocation
Target states with highest readmission rates (MA, NJ, MS, etc.)

### 4. Comprehensive Post-Discharge Care
Develop standardized protocols across all six tracked conditions

### 5. Proactive Patient Screening
Use model to score individual patient readmission risk before discharge

## Technologies Used

- **Python**: pandas, numpy, scikit-learn, matplotlib, seaborn
- **Machine Learning**: Classification models, feature engineering, model evaluation
- **Statistical Analysis**: Hypothesis testing, correlation analysis
- **Data Visualization**: Charts, graphs, and business dashboards

## Files in This Repository

- `01_data_exploration_and_cleaning.ipynb`: Complete analysis notebook
- `hospital_readmissions_cleaned.csv`: Processed dataset
- `readmission_prediction_model.pkl`: Trained Gradient Boosting model
- `feature_importance.csv`: Feature importance rankings
- `project_summary.csv`: Key metrics summary
- `PROJECT_SUMMARY.txt`: Detailed project documentation
- `README.md`: This file

## Future Improvements

- Patient-level analysis using MIMIC-III dataset
- Time series forecasting of readmission trends
- Interactive dashboard for hospital administrators
- Integration with electronic health records (EHR) systems
- Cost-benefit analysis of specific intervention programs

## About the Author

**Sai Mudragada**  
Master's in Business Analytics | Data Science & ML Engineering  
[LinkedIn](#) | [Portfolio](#) | [Email](#)

---

*This project was created as part of a data science portfolio to demonstrate skills in healthcare analytics, machine learning, and business impact analysis.*