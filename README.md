# Hipparcos Classification Model

A machine-learning project exploring the classification of stars using data from the Hipparcos catalogue. The analysis is implemented in a Jupyter notebook and uses **XGBoost** as its primary classifier, with scikit-learn utilities for data preparation and evaluation.

## Project contents

- [`HipporcasModelProject.ipynb`](HipporcasModelProject.ipynb) — notebook containing the data analysis and model workflow.
- `hipparcos-voidmain.csv` — input catalogue expected by the notebook.

## Dataset

The notebook loads the CSV into a pandas DataFrame. Its displayed preview contains **90,643 records and 78 columns**, including astrometric measurements and catalogue identifiers. The data also includes stellar spectral-type information (`SpType`) and a spectral-type reference field (`r_SpType`). The notebook's exact target construction and feature selection should be reviewed in the relevant cells before interpreting model outputs.

## Run the notebook

1. Clone or download this repository and make sure `hipparcos-voidmain.csv` is available in the notebook's working directory. In Google Colab, upload the CSV or mount storage containing it.
2. Open `HipporcasModelProject.ipynb` in Jupyter or Google Colab.
3. Install the notebook dependencies if they are not already available:

   ```bash
   pip install numpy pandas matplotlib scikit-learn xgboost
   ```

4. Run the notebook cells from top to bottom.

The notebook imports XGBoost, pandas, NumPy, Matplotlib, and scikit-learn components for splitting data, imputing missing values, building pipelines, and evaluating classification. It also imports evaluation tools including accuracy, F1 score, a classification report, and a confusion matrix. The notebook includes a cell to upgrade XGBoost.

## Notes

- The CSV is read using the relative path `hipparcos-voidmain.csv`; execution will fail unless the file is in the current working directory or the path is adjusted.
- The notebook imports `RandomForestClassifier` as well as `XGBClassifier`; XGBoost is identified as the main model in the notebook.
- No performance figures are reported here because results depend on the notebook's data preparation, train/test split, and execution environment.
