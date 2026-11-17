# Practical Work No. 5 — Aggregation and Grouping

This repository contains the solution to the practical work on aggregation and
grouping in Pandas: `groupby`, `agg`, `pivot_table`, `crosstab`, and combining
datasets with `merge`, `concat` and `join`.

## Files

| File | Description |
|------|-------------|
| `Surname_Lb5.ipynb` | Practical part, Steps 1–10 (coffee sales dataset). |
| `Surname_Lb5_individual.ipynb` | Individual tasks 1–7 and the bonus task (★). |
| `README.md` | This file. |

> Replace `Surname` in the notebook names with your own surname in English
> (e.g. `Petrenko_Lb5.ipynb`, `Petrenko_Lb5_individual.ipynb`).

## Requirements

- Python 3.9+
- `pandas`, `numpy`
- Jupyter Notebook / JupyterLab, or Google Colab

## How to run

**Google Colab**
1. Upload `sales.csv` to the root of your Google Drive (`MyDrive`).
2. Open a notebook in Colab and run all cells. Google Drive is mounted
   automatically.

**Local Jupyter**
1. Put `sales.csv` next to the notebooks.
2. Run all cells. Output files are written to the `results/` folder.

If `sales.csv` is not found, the notebooks generate a small demo dataset with the
same columns (`date`, `datetime`, `cash_type`, `card`, `money`, `coffee_name`),
so every cell still runs. Run them with the real `sales.csv` before submitting.

## Contents

### `Surname_Lb5.ipynb` — practical part

1. Environment setup and data loading
2. Grouping by one column (`sum`, `mean`)
3. Grouping by several columns (`size`, `reset_index`)
4. Several aggregations with `agg`
5. Pivot table (`pivot_table`)
6. Cross-tabulation (`crosstab`)
7. `merge` (left join with a categories table)
8. `concat`
9. `join` (index-based)
10. Revenue share of each drink

### `Surname_Lb5_individual.ipynb` — individual tasks

| Task | Summary |
|------|---------|
| 1 | Number of transactions per payment type (`Series`). |
| 2 | Max and min transaction amount per drink with `agg()`. |
| 3 | Pivot table: `cash_type` x `coffee_name`, sum of `money`, NaN filled with 0. |
| 4 | Crosstab: `day_of_week` x payment type. |
| 5 | `merge` with a cost table, new column `profit = money - cost`. |
| 6 | `concat` of two artificial DataFrames; index preservation check. |
| 7 | Average check for each hour of the day. |
| ★ | Own dataset with several tables, `concat` + `merge`, grouping with three aggregates, pivot table, results saved to CSV. |

## Output files (bonus task)

Created in the `bonus/` subfolder of the output directory:

- `bonus_merged.csv` — merged dataset
- `bonus_summary.csv` — grouped result (sum, mean, count)
- `bonus_pivot.csv` — pivot table

The assignment asks to commit these CSV files to your GitHub repository in the
appropriate directory.
