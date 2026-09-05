# Assignment 4 — PCA Component Selection

## Main submission
`Assignments/Assignment4_PCA_Components.ipynb`

The notebook is executed top-to-bottom with outputs visible and follows the PDF requirements for Sections 4.1–4.4. It also includes the optional RandomForestRegressor bonus.

## Dataset
`data/raw/pca_regression_data.csv`

## Key result
Using `random_state=42`, the 60-feature Linear Regression baseline has test R² ≈ **0.858373**. The smallest required PCA count meeting the assignment's rule is **8 components**, with test R² ≈ **0.871584**.

## Run
From the project root:
```bash
pip install -r requirements.txt
jupyter notebook Assignments/Assignment4_PCA_Components.ipynb
```

The dataset path is relative to the project root.
