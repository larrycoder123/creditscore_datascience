# Credit Score Classification

A comprehensive machine learning project that predicts customer credit scores (Poor, Standard, or Good) by analyzing credit-related financial behaviors. Compares multiple classification approaches including logistic regression and ensemble methods to identify key indicators of creditworthiness.

## Overview

This project develops and benchmarks predictive models to classify individuals into credit score categories based on financial behaviors and credit history. The analysis explores feature importance, performs extensive data cleaning, and evaluates four distinct modeling approaches to determine the most effective classification method.

**Dataset**: 100,000 observations representing 12,500 customers across 8 months, with 21 features including payment history, debt levels, credit utilization, and financial demographics.

## Key Features

- **Comprehensive Data Cleaning**: Systematic handling of encoded missing values, outlier detection using IQR methods, and feature engineering
- **Multi-Model Comparison**: Benchmarking of Multinomial Logistic Regression, Ordinal Logistic Regression, Decision Trees, and Random Forest
- **Feature Importance Analysis**: Identification of key predictors aligned with real-world credit scoring factors (FICO)
- **Performance Evaluation**: Macro-averaged precision, recall, and F1-scores for multi-class assessment

## Tech Stack

**Languages & Core Libraries**
- R, dplyr, tidyr

**Machine Learning & Modeling**
- nnet (Multinomial Logistic Regression)
- MASS (Ordinal Logistic Regression)
- rpart (Decision Trees)
- ranger (Random Forest)

**Data Visualization**
- ggplot2, patchwork

**Development**
- R Markdown (reproducible reports)

## Project Structure

```
code/
├── creditscore_project.Rmd          # Complete analysis & modeling workflow
├── creditscore_project.html         # Knitted HTML report
├── data/
│   ├── train.csv                    # Original dataset
│   └── train_cleaned.csv            # Processed dataset
└── README.md
```

## Key Findings

- **Model Performance**: Random Forest achieved the best results with 81.2% accuracy, significantly outperforming the 53.1% baseline
- **Top Predictors**: Credit Mix, Outstanding Debt, and Interest Rate emerged as the most important features for classification
- **Real-World Alignment**: Key predictors align closely with FICO credit score components (Payment History 35%, Amount Owed 30%, Credit Mix 10%)
- **Comparison Insights**: 
  - Random Forest: 81.2% accuracy, 80.2% F1-score
  - Decision Tree: 68.8% accuracy, 66.9% F1-score  
  - Multinomial Logistic: 65.9% accuracy, 63.7% F1-score
  - Ordinal Logistic: 63.2% accuracy, 54.5% F1-score

## Documentation

- **Full Report**: [Interactive HTML Report](https://larrycoder123.github.io/creditscore_datascience/code/creditscore_project.html)
- **Project Overview**: See `project_overview.pdf` for methodology, metrics, and detailed takeaways

## Dataset

**Source**: [Credit Score Classification](https://www.kaggle.com/datasets/parisrohan/credit-score-classification) by Rohan Paris  
**License**: CC0: Public Domain

The dataset includes variables across five key categories:
- **Payment History**: Payment delays, minimum payment indicators, payment behavior
- **Amount Owed**: Outstanding debt, credit utilization ratio, total EMI
- **Credit History**: Age of credit history
- **New Credit**: Number of credit inquiries
- **Credit Mix**: Diversity of credit account types

---

*This project demonstrates end-to-end machine learning workflow including data preprocessing, exploratory analysis, model selection, and interpretation of results in the context of real-world credit scoring systems.*
