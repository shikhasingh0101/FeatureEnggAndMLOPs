# Assignment 5 — Data Leakage

Completed submission package for **Feature Engineering & MLOps — Assignment 5: Catching Data Leakage Before It Catches You**.

## Included

```text
Assignment5_DataLeakage/
├── Assignments/
│   └── Assignment5_DataLeakage.ipynb
├── data/
│   └── raw/
│       └── customer_churn_a5.csv
├── README.md
└── requirements.txt
```

## Notebook

`Assignments/Assignment5_DataLeakage.ipynb` is already executed top-to-bottom with outputs embedded.

It covers:

- **4.1 Target leakage:** post-cancellation fields, correlation, honest Model A, leaked Model B, accuracy/ROC-AUC gap, production explanation.
- **4.2 Preprocessing leakage:** whole-dataset scaler vs. training-only scaler, numeric mean differences, and a correct sklearn Pipeline.
- **4.3 The fix:** final deployable pipeline using only legitimate features and train-only preprocessing.
- **Bonus:** 5-fold cross-validation comparison of leaky preprocessing vs. preprocessing inside the CV pipeline.

## Main results

- Dataset: 600 customers
- `days_since_cancellation` non-null rows: **149**
- `churn = 1` rows: **149**
- Correlation of filled `final_bill_amount` with `churn`: **0.924978**
- Correlation of `tenure_months` with `churn`: **-0.220718**
- Model A test accuracy: **0.753333**
- Model A ROC-AUC: **0.778283**
- Model B test accuracy: **1.000000**
- Model B ROC-AUC: **1.000000**
- Accuracy gap: **0.246667**
- ROC-AUC gap: **0.221717**

The notebook uses `random_state=42`, a 75/25 stratified train/test split, and Logistic Regression.

## Install and run

```bash
pip install -r requirements.txt
jupyter notebook Assignments/Assignment5_DataLeakage.ipynb
```

## GitHub submission

From the course repository root, place the notebook in the top-level `Assignments` folder and run:

```bash
git add Assignments/Assignment5_DataLeakage.ipynb
git commit -m "Assignment 5: Target and preprocessing leakage"
git push
```
