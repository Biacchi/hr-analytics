# hr-analytics

A basic HR analytics notebook: plots, a correlation heatmap, and a first attempt at predicting employee attrition with a random forest. Think "my first date with machine learning", nothing fancy.

## Why it exists

A practice project from my data-analysis learning days, built on the well-known (and fictional) IBM HR Analytics Attrition dataset. No real employees were harmed, or even involved.

## Where the data comes from

The notebook reads `WA_Fn-UseC_-HR-Employee-Attrition.csv` from the Kaggle dataset **IBM HR Analytics Employee Attrition & Performance**. The CSV is **not** in this repo, so download it from Kaggle first.

## How to run it

```bash
pip install -r requirements.txt
jupyter lab hr-analytics.ipynb
```

Then update the `pd.read_csv(...)` path in the first code cell (it points at the Kaggle path `/kaggle/input/...`).

## What is in here

- `hr-analytics.ipynb`: the analysis
- `requirements.txt`: the libraries the notebook imports

## What the notebook does

1. Loads the data and prints the usual `head`, `describe` and `info`.
2. Plots monthly income, age, age vs. income, headcount per department and per education field.
3. Draws a correlation heatmap of the numeric columns.
4. Trains a `RandomForestClassifier` (80/20 split, `random_state=42`) to predict `Attrition` and prints accuracy, a confusion matrix and a classification report.

The notebook was saved without outputs, so there are no results to quote here. Run it to see the numbers.

## What I learned

How to go from "I have a CSV" to "I have a model" in one notebook, and that one-hot encoding a pile of categorical columns is easier than it sounds.

## Heads-up

- No license file yet, so by default all rights are reserved.
- I have not re-run the notebook after tidying the repo.
