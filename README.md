## Factors Associated with Life Satisfaction Among Women in Canada
**Overview**

This repository contains the code, documentation, exploratory analysis, figures, tables, and project report for my Major Research Project (MRP) in the MSc Data Science and Analytics program at Toronto Metropolitan University.

The study investigates factors associated with life satisfaction among women in Canada using data from the 2022 Canadian Community Health Survey (CCHS). The project focuses on demographic, socioeconomic, employment-related, and health-related determinants of subjective well-being. It uses exploratory data analysis, statistical testing, and interpretable data analytics methods to identify factors associated with lower life satisfaction.

**Research Objective**

The primary objective of this study is to examine how demographic characteristics, socioeconomic conditions, employment-related factors, and health-related factors are associated with life satisfaction among women in Canada.

The study aims to:

•	Explore patterns of life satisfaction among women in Canada.
•	Identify factors associated with lower life satisfaction.
•	Examine the role of income, food security, employment status, education, functional difficulty, and chronic health conditions.
•	Apply interpretable predictive modeling methods, including Logistic Regression and Decision Tree Classification.


## Dataset

**Data Source**: Canadian Community Health Survey (CCHS) 2022
**Provider**: Statistics Canada
**Study Population**: Female respondents only
**Final Exploratory Analysis Sample**: 52,884 women

Due to Statistics Canada licensing and data-sharing restrictions, the CCHS 2022 Public Use Microdata File is not included in this repository. The data/README.md file provides information about the dataset source and data access limitations.



## Repository Structure

MRP_CCHS_2022

├── notebooks/
│   ├── 01_data_preparation.ipynb
│   └── 02_exploratory_data_analysis.ipynb
│
├── outputs/
│   ├── figures/
│   └── tables/
│
├── report/
│   ├── MRP_Literature_Review_EDA_June2026.pdf
│   └── references.bib
│
├── data/
│   └── README.md
│
└── README.md


## Current Progress

**Completed**
Literature review
Data preparation
Variable selection
Data cleaning
Exploratory Data Analysis (EDA)
Visual analysis of life satisfaction patterns
Chi-square tests and Cramer's V association analysis
Project methodology design
Workflow diagram
June 2026 literature review and EDA deliverable

**Planned**
Logistic Regression modeling
Decision Tree Classification
Model evaluation
Interpretation of predictors
Final report and conclusions

## Key Variables
**Outcome Variable**
Life Satisfaction (LSMDVSWL)

**Predictor Categories**
Demographic factors
Socioeconomic factors
Employment-related factors
Health-related factors

**Key predictors include:**

Age group
Household income
Education level
Household food security
Labour force status
Functional difficulty
Musculoskeletal chronic condition
Province of residence
Immigrant status
Visible minority status

## Methods

The project currently includes descriptive statistics, exploratory data analysis, visual comparison of low life satisfaction across key groups, and statistical testing using Chi-square tests and Cramer's V. The next stage of the project will apply interpretable predictive modeling methods, including Logistic Regression and Decision Tree Classification.

Model performance will be evaluated using accuracy, precision, recall, F1-score, weighted F1-score, and ROC-AUC, with attention to class imbalance in the lower life satisfaction outcome.

## Tools and Technologies
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
Jupyter Notebook
LaTeX
GitHub
 
## Deliverable
The current June 2026 deliverable is available in the report/ folder:
report/MRP_Literature_Review_EDA_June2026.pdf

## Author

**Khushboo Singh**
MSc Data Science and Analytics
Toronto Metropolitan University

## Supervisor

**Dr. Ozgur Turetken, Ph.D.**
Professor, Information Technology Management
Ted Rogers School of Management
Toronto Metropolitan University
Ted Rogers School of Management

Toronto Metropolitan University

