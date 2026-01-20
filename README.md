Labor Market Analytics in Kazakhstan: Vacancy and Salary Trends
Overview

This project analyzes the labor market in Kazakhstan using job vacancy data collected from Enbek.kz, the official employment platform of Kazakhstan. The dataset includes 21,929 job postings published between July 16, 2024, and December 7, 2024. The project focuses on salary distributions, regional differences, professional areas, education and experience requirements, as well as temporal and seasonal hiring patterns. A machine learning pipeline is also developed to explore the feasibility of predicting minimum salaries based on vacancy attributes.

The study provides actionable insights for job seekers, employers, policymakers, and anyone interested in understanding Kazakhstan's labor market dynamics.

Project Objectives

Clean and structure job vacancy data from Enbek.kz.

Analyze salary distributions and identify outliers.

Study regional, professional, educational, and experience-based salary differences.

Explore temporal patterns such as weekday and seasonal trends.

Visualize regional salary differences using geographic maps.

Build and evaluate machine learning models for predicting minimum salary.

Novelty & Originality

Integrated Analytical Pipeline: Combines data cleaning, feature engineering, exploratory analysis, geospatial visualization, and machine learning in a single workflow.

Custom Feature Extraction: Converts textual experience requirements into numeric values for quantitative analysis.

Regional Salary Visualization: Uses administrative region polygons to highlight spatial inequalities in salaries.

Critical Model Evaluation: Identifies target leakage in salary prediction models and treats predictive modeling as an analytical experiment rather than a black-box solution.

Dataset

Source: Job postings from Enbek.kz and administrative boundaries of Kazakhstan (GeoJSON).

Coverage: July 16, 2024 – December 7, 2024

Size: 21,929 job postings, 20 features

Key Features: Job Title, Professional Area, Company, Work Type, Experience Required, Education Required, Salary Min/Max, Region, Posting Date, Day of Week, Month, Season, and engineered salary-related features.

Data Preprocessing

Experience normalization: “Без опыта” → 0 years; numeric extraction from text-based experience.

Datetime processing: Extracted day of week, month, and season from posting dates.

Salary features: Calculated salary range and ratio; used Z-scores to detect outliers.

Encoding: One-hot encoding for categorical variables, resulting in 67 features.

Exploratory Data Analysis

Salary Distribution: Right-skewed, with mean ≈ 159,595 KZT and median ≈ 140,000 KZT.

Regional Differences: Highest salaries in Astana and Almaty; industrial regions like Karaghandy and Qostanay also above average.

Professional Areas: Oil & gas, engineering, and management roles offer highest pay.

Experience vs Salary: Positive correlation; salary growth stabilizes after ~6–7 years.

Temporal Patterns: Most vacancies posted on Mondays and Tuesdays; peak hiring in Autumn and Winter.

Education Requirements: Higher education correlates with higher salaries; vocational/secondary education more common in service/unskilled roles.

Visualizations

Bar Charts: Vacancies by day of week, seasonal trends, top locations.

Scatter Plots: Experience vs minimum salary.

Box Plots: Salary vs education level.

Histograms: Salary distribution (min/max).

Choropleth Maps: Regional salary differences.

Line Charts: Vacancy trends over time.

Machine Learning

Task: Predict minimum salary based on vacancy attributes.

Models Tested: Linear Regression, Ridge (L2), Lasso (L1), Random Forest, Gradient Boosting.

Target Leakage: Identified features derived from salary itself, which inflated performance metrics.

Evaluation Metrics: R², MAE, RMSE.

Key Findings

Strong regional and professional salary disparities.

Experience is a major determinant of salary.

Clear temporal patterns in posting activity by weekday and season.

Higher education is associated with higher salaries.

Outlier salaries often correspond to niche or high-demand roles.

Limitations

Salary data may contain outliers or broad ranges rather than exact values.

Regional name alignment required careful preprocessing.

Limited explanatory variables for salary prediction.

Target leakage affected initial machine learning models.

Future Work

Implement more robust salary range handling.

Extract additional features from job titles and descriptions.

Apply NLP techniques on vacancy descriptions for richer modeling.

Conduct fairness and bias analysis for regional and professional categories.

Improve model validation using time-based splits and cross-validation.

Conclusion

This project demonstrates practical data analytics skills and the ability to derive meaningful insights from real-world labor market data. It provides a comprehensive overview of Kazakhstan’s job market, combining exploratory analysis, geospatial visualization, and machine learning experimentation. The study highlights key salary patterns, regional inequalities, and temporal trends, offering valuable information for job seekers, employers, and policymakers.
