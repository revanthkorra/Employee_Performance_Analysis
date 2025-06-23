# Employee_Performance_Analysis
#  Employee Performance Prediction using Machine Learning

This project analyzes employee data from *INX Future Inc.* to predict performance ratings using advanced machine learning techniques. It aims to help HR identify potential performance issues and make data-driven workforce decisions without affecting team morale.



##  Problem Statement

Mr. Brain, an HR leader and data scientist, wants to discover patterns in employee data to understand the *core factors* influencing low or high performance ratings. The ultimate goal is to enable *early intervention* for underperforming employees and guide reward policies for top performers.



##  Dataset

*Source*: [INX Future Inc. Employee Dataset] (http://data.iabac.org/exam/p2/data/INX_Future_Inc_Employee_Performance_CDS_Project2_Data_V1.8.xls)
- Number of records: ~1200
- Target variable: PerformanceRating (2, 3, or 4)
- Features: Age, Department, Education, JobRole, Overtime, Attrition, etc.



##  Project Structure
- Employee_Performance_Project/
- ├── data/
- │ ├── raw/ # Original XLS dataset
- │ ├── processed/ # Scaled and clean data for ML
- │ └── external/ # Any third-party references
- │
- ├── src/
- │ ├── Data Processing/
- │ │ ├── data_processing.ipynb
- │ │ └── data_exploratory_analysis.ipynb
- │ ├── models/
- │ │ ├── train_model.ipynb
- │ │ └── predict_model.ipynb
- │ └── visualization/
- │ └── visualize.ipynb
- │
- ├── references/
- │ ├── data_dictionary.md
- │ └── INX_dataset_link.txt
- │
- ├── reports/
- │ └── figures/ # SHAP summary, bar charts, waterfall plots
- │
- ├── Project Summary/
- ├── Requirement/
- ├── Analysis/
- ├── Summary/





##  Models Used

| Model        | Accuracy | F1 Macro Score |
|--------------|----------|----------------|
| XGBoost      | 91.67%   | 0.8785         |
| RandomForest | ~88%     | ~0.84          |
| DecisionTree | ~83%     | ~0.78          |

- Final model selected:  *XGBoost*
- Labels remapped: 2 → 0, 3 → 1, 4 → 2



##  SHAP Explainability

SHAP (SHapley Additive exPlanations) was used to:
- Interpret feature importance globally
- Understand local instance-level decisions
- Generate summary, bar, interaction, and waterfall plots

## Top impactful features:
- OverTime
- EmpJobRole
- EmpEnvironmentSatisfaction

## Sample Results
###  Classification Report

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| *2*   | 0.79      | 0.85   | 0.81     |  39     |
| *3*   | 0.94      | 0.95   | 0.95     |  175    |
| *4*   | 0.95      | 0.81   | 0.88     |  26     |

Accuracy: 0.92
F1 Macro Score: 0.88

## References
- references/data_dictionary.md – explains all feature meanings.

Contact
- Author: Revanth Korra
- Email: revanthvirat183@gmail.com
- LinkedIn : https://www.linkedin.com/in/korra-revanth-3aa2082a9/
