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
│   └── 01_data_preparation.ipynb            # P4 & M2: gathering, cleaning, encoding, splitting, scaling
├── reports/
│   ├── fig1_class_and_bmi_before.png
│   └── fig2_train_test_balance_after.png
├── requirements.txt
└── README.md
```

## Project Status

- [x] P3 — Objectives defined
- [x] P4 — Data gathered and prepared
- [x] M2 — Dataset reviewed and refined, with justified choices
- [ ] P5 — Model development (Task 3)
- [ ] M3 — Model testing and refinement (Task 3)
- [ ] D2 — Effectiveness evaluation (Task 3)

## Author

Ethan Ngari — BTEC International Level 3 Diploma in IT
