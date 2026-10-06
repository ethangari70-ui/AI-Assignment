# Stroke Prediction AI Solution — Nairobi Smart Solutions Ltd.

BTEC Unit 21 (Introduction to Artificial Intelligence) coursework project. Built as a junior AI developer scenario for Nairobi Smart Solutions Ltd., demonstrating how AI can be applied to predict stroke risk from patient health data.

## Project Overview

This project uses the [Healthcare Stroke Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset) (Kaggle, author: fedesoriano) to build a Logistic Regression model that predicts a patient's risk of stroke based on demographic, lifestyle, and health data.

Given the severe class imbalance in the dataset (only 4.87% of patients had a stroke), the project prioritises **recall for the stroke class** over raw accuracy — a model that never predicts a stroke would already be ~95% "accurate" while being clinically useless.

## Repository Structure

```
stroke_project/
├── data/
│   ├── healthcare-dataset-stroke-data.csv   # raw dataset
│   ├── stroke_data_processed.csv            # cleaned/encoded dataset
│   ├── X_train.csv / X_test.csv             # prepared, scaled features
│   └── y_train.csv / y_test.csv             # target labels
├── notebooks/
│   ├── 01_data_preparation.ipynb            # P4 & M2: gathering, cleaning, encoding, splitting, scaling
│   └── 02_model_building.ipynb              # P5, M3 & D2: model training, testing, refinement, evaluation
├── reports/
│   ├── fig1_class_and_bmi_before.png
│   ├── fig2_train_test_balance_after.png
│   ├── fig3_confusion_matrix_baseline.png
│   ├── fig4_confusion_matrix_refined.png
│   ├── fig5_baseline_vs_refined_comparison.png
│   ├── fig6_threshold_tuning.png
│   ├── fig7_confusion_matrix_final.png
│   ├── fig8_roc_curve_final.png
│   └── fig9_feature_importance.png
├── requirements.txt
└── README.md
```

## Results Summary

The final Logistic Regression model (trained with `class_weight='balanced'`, decision threshold tuned to 0.70) achieved, on the held-out test set:

- **Recall (stroke class): 72.0%** — correctly identified 36 of 50 stroke cases
- **Precision (stroke class): 20.2%**
- **Accuracy: 84.7%**
- **ROC-AUC: 0.840**

## Setup

```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

## Project Status

- [x] P3 — Objectives defined
- [x] P4 — Data gathered and prepared
- [x] M2 — Dataset reviewed and refined, with justified choices
- [x] P5 — Model developed (Logistic Regression)
- [x] M3 — Model tested and refined (class weighting + threshold tuning)
- [x] D2 — Effectiveness evaluated against P3 objectives

## Author

Ethan Ngari — BTEC International Level 3 Diploma in IT
