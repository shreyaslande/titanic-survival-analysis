# Titanic Survival Analysis (EDA)

Exploratory data analysis of the Titanic passenger dataset — who survived, and what factors were linked to survival?

## Dataset

- `data/titanic.csv` — 891 passenger records (the classic Kaggle Titanic training set).
- Columns include survival status, ticket class, sex, age, fare, port of embarkation, and family counts (siblings/spouses, parents/children).

## Data cleaning

- **Cabin** dropped — ~77% of values missing, too sparse to use.
- **Age** — missing values filled with the **median** age (robust to outliers).
- **Embarked** — 2 missing values filled with the most frequent port (S).
- **Fare** — median-filled if missing.

## Key findings

- **Overall survival rate: 38.4%**
- **Gender was the strongest factor:** 74.2% of women survived vs 18.9% of men.
- **Ticket class mattered:** 63.0% survival in 1st class vs 24.2% in 3rd class (2nd class: 47.3%).
- **Fare:** survivors had paid notably higher fares (median roughly double), consistent with the class pattern.
- **Age:** young children had a clear survival advantage; for adults the effect was weaker.

Findings are presented through 5 charts in the notebook: overall survival, survival by gender, survival by class, fare distribution by survival, and age distribution by survival.

## How to run

```bash
pip install -r requirements.txt
jupyter notebook titanic_eda.ipynb
```

The notebook is saved with all outputs and charts embedded, so it can also be read directly on GitHub without running anything.

## Tech stack

Python · Pandas · NumPy · Matplotlib · Seaborn · Jupyter
