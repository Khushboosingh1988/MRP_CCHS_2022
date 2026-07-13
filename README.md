# Factors Associated with Life Satisfaction Among Women in Canada

## Overview

This repository contains the code, documentation, exploratory analysis, figures, tables, and project report for my Major Research Project (MRP) in the MSc Data Science and Analytics program at Toronto Metropolitan University.

The study investigates factors associated with low life satisfaction among women in Canada using data from the 2022 Canadian Community Health Survey (CCHS) Public Use Microdata File. The project focuses on demographic, socioeconomic, employment-related, and health-related factors associated with subjective well-being.

The analysis combines exploratory data analysis, statistical testing, and predictive modeling to examine which factors are most strongly associated with low life satisfaction.

## Research Objective

The primary objective of this study is to examine how demographic characteristics, socioeconomic conditions, employment-related factors, and health-related factors are associated with low life satisfaction among women in Canada.

The study aims to:

- Explore patterns of life satisfaction among women in Canada.
- Identify factors associated with low life satisfaction.
- Examine the role of income, food security, employment status, education, functional difficulty, and chronic health conditions.
- Compare interpretable and ensemble classification models.
- Evaluate model performance under class imbalance.
- Identify predictors that appear consistently important across exploratory and predictive methods.

## Research Questions

This project addresses two main research questions:

1. Which demographic, socioeconomic, employment-related, and health-related factors are associated with low life satisfaction among women in Canada?

2. How well can these variables identify women with low life satisfaction, and which predictors appear consistently important across different classification models?

## Dataset

**Data Source:** Canadian Community Health Survey (CCHS) 2022  
**Provider:** Statistics Canada  
**Data Type:** Public Use Microdata File (PUMF)  
**Study Population:** Female respondents aged 18 years and older  
**Final Exploratory Analysis Sample:** 52,884 women  
**Final Predictive Modeling Sample:** 52,543 women  

The outcome variable is life satisfaction, measured using the CCHS variable `LSMDVSWL`.

For predictive modeling, respondents who reported being **Dissatisfied** or **Very Dissatisfied** were classified as having low life satisfaction. In the final modeling sample, approximately **6.31%** of respondents were classified as having low life satisfaction.

Due to Statistics Canada licensing and data-sharing restrictions, the raw CCHS 2022 Public Use Microdata File is not included in this repository. The `data/README.md` file provides information about the dataset source and data access limitations.

## Repository Structure

MRP_CCHS_2022/

- data/
  - README.md

- notebooks/
  - 01_data_preparation.ipynb
  - 02_exploratory_data_analysis.ipynb
  - 03_predictive_modeling.ipynb

- outputs/
  - figures/
  - tables/

- report/
  

- README.md
- .gitignore

## Key Variables

### Outcome Variable

- Life Satisfaction (`LSMDVSWL`)

### Binary Modeling Outcome

- `LowLifeSatisfaction`

Respondents were coded as follows:

- `1` = Dissatisfied or Very Dissatisfied
- `0` = Very Satisfied, Satisfied, or Neither Satisfied nor Dissatisfied

### Predictor Categories

- Demographic factors
- Socioeconomic factors
- Employment-related factors
- Health-related factors

### Key Predictors

- Age group (`DHHGAGE`)
- Household size (`DHHDGHSZ`)
- Province of residence (`GEOGPRV`)
- Immigrant status (`SDCDGIMM`)
- Visible minority status (`SDCDVFLA`)
- Household income (`INCDGHH`)
- Education level (`EDDVH3`)
- Household food security (`FSCDVHF2`)
- Labour force status / working status last week (`LBFDGWSS`)
- Functional difficulty (`WDMDGDIF`)
- Musculoskeletal chronic condition (`CCCDGSKL`)

Two employment-specific variables, full-time or part-time employment and hours worked per week, were examined during data preparation but were not included in the primary full-sample models because they apply only to employed respondents.

## Methods

The project includes the following analytical stages:

### 1. Data Preparation

- Selected relevant CCHS 2022 variables.
- Filtered the dataset to female respondents.
- Removed invalid, missing, and non-response categories.
- Created a broader women-focused dataset for exploratory analysis.
- Created a cleaned modeling dataset for predictive modeling.

### 2. Exploratory Data Analysis

- Examined the distribution of life satisfaction.
- Compared low life satisfaction across demographic, socioeconomic, employment-related, and health-related groups.
- Created visualizations for key predictors.
- Conducted Chi-square tests of independence.
- Used Cramer's V to assess the strength of association.

### 3. Predictive Modeling

The following classification models were developed and compared:

- Majority-class baseline model
- Logistic Regression
- Decision Tree Classification
- Tuned Decision Tree
- Random Forest
- Tuned Random Forest
- Gradient Boosting

### 4. Model Evaluation

Model performance was evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Weighted F1-score
- Balanced accuracy
- ROC-AUC
- PR-AUC

Because low life satisfaction was an imbalanced outcome, the analysis gave special attention to recall, F1-score, balanced accuracy, and PR-AUC rather than relying only on accuracy.

Validation-based threshold analysis was also conducted using out-of-fold predictions from the training data.

## Key Findings

The exploratory and predictive results were generally consistent.

The strongest and most consistent factors associated with low life satisfaction were:

- Functional difficulty
- Household food insecurity
- Labour force status
- Household income

Food security showed the strongest bivariate association in the exploratory analysis, while functional difficulty was the most consistently important predictor across the predictive models.

The predictive models performed better than the majority-class baseline, but overall performance was moderate. Gradient Boosting achieved the highest held-out PR-AUC, but its improvement over Logistic Regression and Random Forest was small. This suggests that Logistic Regression remained useful because it provided similar predictive performance with clearer interpretation.

## Limitations

Several limitations should be considered:

- The CCHS is cross-sectional, so the findings represent associations rather than causal relationships.
- Many variables are self-reported and may be affected by response or recall bias.
- The Public Use Microdata File groups some variables into broader categories.
- The life satisfaction outcome was converted from five categories into a binary variable for modeling.
- Low life satisfaction was a small class, creating a class imbalance problem.
- No suitable survey-weight variable was available in the processed datasets used in this study, so the descriptive statistics, statistical tests, and predictive models are unweighted.

Therefore, the findings describe patterns within the analytical sample and should not be interpreted as nationally representative estimates for all women in Canada.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- LaTeX
- GitHub

## Current Deliverable

The July 2026 updated MRP report is available in the `report/` folder:

`report/MRP_Project_Experiments_July_14.pdf`

This report includes the literature review, data description, exploratory analysis, methodology, predictive modeling results, discussion, conclusion, and project limitations.

## Data Access Note

The raw CCHS 2022 Public Use Microdata File is not included in this repository. Users who want to reproduce the analysis must obtain an authorized copy of the CCHS 2022 PUMF from Statistics Canada and follow the data access and licensing requirements.

## Author

**Khushboo Singh**  
MSc Data Science and Analytics  
Toronto Metropolitan University

## Supervisor

**Dr. Ozgur Turetken, Ph.D.**  
Professor, Information Technology Management  
Ted Rogers School of Management  
Toronto Metropolitan University
