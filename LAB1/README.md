# Practical Assignment No. 1. Introduction to Data Analytics and Google Colab

## Objective

Learn to create notebooks in the Google Colab cloud environment, load and perform an initial inspection of tabular data with Pandas, and carry out basic vector computations with NumPy.

## Repository Contents

| File | Description |
|------|-------------|
| `Індивідуальне завдання_Гураль.ipynb` | Notebook with solutions to individual tasks 1–7 and the bonus task ★ |
| `README.md` | Short description of the completed work |

## Dataset Used

The test file `test_sales.csv` (12 rows, 5 columns), created programmatically in the notebook. It simulates coffee shop transaction records:

| Column | Description |
|--------|-------------|
| `date` | transaction date |
| `hour` | hour of purchase |
| `payment` | payment type (`card` / `cash`) |
| `drink` | drink name |
| `money` | amount, UAH |

> If a different dataset was used (for example, `sales.csv` provided by the instructor), specify its name here.

## What Was Done

1. Imported `pandas` and `numpy` and printed their versions.
2. Created and read a CSV into a DataFrame, then used `head(3)` and `tail(3)`.
3. Listed the columns (`df.columns`) and checked the type of that object.
4. One-dimensional NumPy array (first 10 even numbers): sum, mean, minimum, maximum, multiplication by 3.
5. Two-dimensional 3×3 array of random integers from 1 to 10, sums along `axis=0` and `axis=1`.
6. Markdown cell with a heading, a list, and bold text, plus an explanation of the benefits of text cells.
7. Mounted Google Drive, read a CSV from Drive, ran `df.info()`, and compared data types.
8. ★ Comprehensive notebook: `head()`, `shape`, `info()`, `describe()`, converting the `money` column to a NumPy array (`to_numpy()`) and computing its mean.

## Tools

- Python 3
- Google Colab
- pandas
- NumPy
