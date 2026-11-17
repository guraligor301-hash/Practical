# Practical Work No. 3 — Data Cleaning and Transformation

This repository contains the solution to Practical Work No. 3 (Pandas / NumPy):
detecting and handling missing values, duplicates and outliers; converting data
types; working with string and datetime values; feature engineering; one-hot
encoding; normalization and standardization; and building a reproducible
cleaning pipeline.

## Files

| File | Description |
|------|-------------|
| `Surname_Lb3.ipynb` | Practical part, Steps 1–10 (coffee sales dataset). |
| `Surname_Lb3_individual.ipynb` | Individual tasks 1–7 and the bonus task 8 (★). |
| `README.md` | This file. |

> Rename the notebooks by replacing `Surname` with your own surname in English
> (e.g. `Petrenko_Lb3.ipynb`, `Petrenko_Lb3_individual.ipynb`).

## Requirements

- Python 3.9+
- `pandas`, `numpy`
- Jupyter Notebook / JupyterLab, or Google Colab

## How to run

**Google Colab**
1. Upload `sales.csv` to the root of your Google Drive (`MyDrive`).
2. Open a notebook in Colab and run all cells. Google Drive is mounted
   automatically; results are saved to `MyDrive`.

**Local Jupyter**
1. Put `sales.csv` next to the notebooks.
2. Run all cells. Results are saved to the `results/` folder (created automatically).

If `sales.csv` is not found, the notebooks generate a small demo dataset with the
same columns (`date`, `datetime`, `cash_type`, `card`, `money`, `coffee_name`),
so every cell still runs. Run the notebooks with the real `sales.csv` before
submitting, so the outputs match your actual data.

## Contents

### `Surname_Lb3.ipynb` — practical part

1. Environment setup and data loading
2. Missing values (`isnull`, `dropna`, `fillna`)
3. Duplicates (`duplicated`, `drop_duplicates`)
4. Outliers (IQR method)
5. Data type conversion (`pd.to_datetime`)
6. String cleaning (`.str.strip`, `.str.lower`, `.str.replace`)
7. Feature engineering with `.dt` (hour, day of week, month)
8. One-hot encoding (`pd.get_dummies`)
9. Normalization (min-max) and standardization (z-score)
10. Saving the cleaned data to `cleaned_sales.csv`

### `Surname_Lb3_individual.ipynb` — individual tasks

| Task | Summary |
|------|---------|
| 1 | Synthetic DataFrame (6 columns) with NaNs, duplicates and outliers; fill with median/mode, drop duplicates, filter outliers by IQR. |
| 2 | Add 5 NaNs to `money` and 3 duplicates in `sales.csv`; clean, convert `datetime`, save a new CSV. |
| 3 | Year, month, day, day-of-week and hour features from `datetime`; first 10 rows. |
| 4 | City and phone string cleaning. |
| 5 | One-hot encoding of `cash_type` with an interpretation of the binary columns. |
| 6 | Min-max normalization and standardization of `money`, with verification checks. |
| 7 | `is_card` feature via `np.where()`. |
| 8 ★ | `clean_dataset(df)` function, tested on a synthetic dirty dataset and saved to CSV. |

## Output files

| File | Created by |
|------|-----------|
| `cleaned_sales.csv` | Practical part, Step 10 |
| `cleaned_sales_task2.csv` | Individual task 2 |
| `cleaned_dataset_task8.csv` | Individual task 8 |

## Notes

- All steps are written in code with comments, so the cleaning sequence is reproducible.
- In task 2, duplicates are removed *before* filling NaNs with the mean, so the
  injected duplicates do not distort the mean.
- In task 8, rows with outliers are removed based on IQR limits computed for every
  numeric column after missing values are filled.
