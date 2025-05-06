# Reducing Dropout Rates in Online Learning Platforms  
**A Predictive and Recommender System Using Machine Learning**  

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange)](https://jupyter.org/)

## Table of Contents
- [Project Overview](#-project-overview)
- [Key Features](#-key-features)
- [Dataset](#-dataset)
- [Project Structure](#-project-structure)
- [Methodology](#-methodology)
- [Results](#-results)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#-usage)
- [Authors](#-authors)
- [License](#-license)
- [Acknowledgments](#-acknowledgments)

## Project Overview
This project addresses the critical challenge of high dropout rates in online learning platforms by:
1. Developing a **predictive model** to identify at-risk students early
2. Building a **personalized recommender system** to provide targeted interventions

The system leverages machine learning techniques on the Open University Learning Analytics Dataset (OULAD) to improve student retention in MOOC platforms.

## Key Features
- **Predictive Modeling**: 
  - Multiple algorithms tested (XGBoost, Random Forest, SVM, etc.)
  - SMOTE for handling class imbalance
  - Hyperparameter tuning for optimal performance
- **Recommender System**:
  - Student risk segmentation (Low Engagement, Low Performance, High Difficulty)
  - Personalized intervention strategies
- **Comprehensive Evaluation**:
  - ROC-AUC: 0.94
  - Recall@89% for at-risk students

## Dataset
We use the **Open University Learning Analytics Dataset (OULAD)** which contains:
- Student demographics and socioeconomic status
- Course registration details
- Assessment results
- VLE (Virtual Learning Environment) interactions

Dataset Tables:
1. `studentInfo.csv` - Student demographics
2. `studentRegistration.csv` - Enrollment records
3. `courses.csv` - Course details  
4. `assessments.csv` - Assessment information  
5. `studentAssessment.csv` - Student assessment results  
6. `studentVle.csv` - VLE interactions  
7. `vle.csv` - VLE resource information  

## Project Structure
├── data/ # Data directories
│ ├── raw/ # Raw original data (.gitignored)
│ └── processed/ # Processed data (.gitignored)
│
├── notebooks/ # Jupyter notebooks
│ ├── 1_Data_Processing.ipynb
│ ├── 2_EDA.ipynb
│ ├── 3_Model_Training.ipynb
│ └── 4_Recommendation_System.ipynb
│
├── src/ # Python scripts
│ ├── data_processing.py
│ ├── models.py
│ └── evaluation.py
│
├── docs/ # Documentation
│ └── Project_Report.pdf # Full project report
│
├── results/ # Outputs
│ ├── figures/ # Visualizations
│ └── metrics/ # Performance metrics
│
├── .gitignore
├── LICENSE
├── README.md # This file
└── requirements.txt # Dependencies

## Methodology
### Predictive Modeling Workflow
1. **Data Preprocessing**:
   - Merging multiple data sources
   - Feature engineering (engagement metrics, performance indicators)
   - Handling missing values and outliers
   
2. **Model Development**:
   - Algorithm comparison (XGBoost outperformed with 89% recall)
   - Hyperparameter tuning
   - 5-fold cross-validation

3. **Evaluation Metrics**:
   - Focus on Recall for at-risk class
   - Precision-Recall tradeoff analysis
   - ROC-AUC measurement

### Recommender System Approach
1. **Student Segmentation**:
   - Low Engagement
   - Low Performance 
   - High Difficulty

2. **Intervention Strategies**:
   - Personalized resource recommendations
   - Study plan adjustments
   - Support system connections

## Results
| Model               | Accuracy | Precision (At-Risk) | Recall (At-Risk) | F1-Score |
|---------------------|----------|---------------------|------------------|----------|
| Logistic Regression | 85%      | 0.50                | 0.86             | 0.64     |
| Random Forest       | 85%      | 0.50                | 0.74             | 0.66     |
| **XGBoost**         | **89%**  | **0.64**            | **0.60**         | **0.64** |



## Getting Started
### Prerequisites
- Python 3.8+
- Jupyter Notebook
- pip package manager

### Installation
1. Clone the repository:
```bash
git clone https://github.com/oumaimaatmani/MOOC-Analysis.git
cd MOOC-Analysis
