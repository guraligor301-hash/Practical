# Practical Work No. 2. Pandas: Working with Tables

**Notebook:** `Surname_Practice2.ipynb` (Google Colab)

## Goal
Learn the core Pandas structures (`DataFrame` and `Series`) and practice importing data from files, inspecting it, indexing, filtering and sorting tabular data.

## What was done
- **Steps 1–8 of the practical part:** creating a DataFrame from a dictionary, importing `sales.csv`, `info()` / `describe()`, indexing with `loc` / `iloc`, filtering with boolean masks, sorting, saving results to CSV.
- **Individual tasks 1–7:**
  1. A custom DataFrame with three favorite books (`title`, `author`, `year`, `rating`).
  2. First and last 3 rows with `head(3)` / `tail(3)`.
  3. Column names via `df.columns` and the type of that object.
  4. `loc` and `iloc` examples.
  5. Filtering by `cash_type == 'card'` and counting the remaining rows.
  6. Filtering `Latte` transactions with `money > 30`.
  7. Sorting by `datetime` in chronological order.
- **Bonus task (★):** the function `count_by_category(df, column)` built on `value_counts()` and `sort_values()`, demonstrated on `coffee_name`.
- Answers to the self-check questions.

## Dataset
`sales.csv` — coffee sales data with the columns:

| Column | Description |
|---|---|
| `date` | Date of the transaction (text) |
| `datetime` | Date and time of the transaction (text, converted to datetime when sorting) |
| `cash_type` | Payment type (`card` / `cash`) |
| `card` | Anonymized card identifier (empty for cash payments) |
| `money` | Transaction amount |
| `coffee_name` | Name of the drink |

## How to run
1. Open the notebook in Google Colab.
2. Make `sales.csv` available in one of two ways:
   - **Google Drive:** upload `sales.csv` to the root of "My Drive" and run the `drive.mount('/content/drive')` cell.
   - **Direct upload:** run `from google.colab import files; files.upload()`, select `sales.csv`, and change the paths in the notebook from `/content/drive/MyDrive/sales.csv` to `sales.csv`.
3. Run all cells from top to bottom (`Runtime → Run all`). The first cell with the imports must be executed before any other code.

## Output files
- `filtered_sales.csv` — transactions with `money > 35`, sorted in descending order.
- `coffee_counts.csv` — number of records per `coffee_name` (bonus task).

## Requirements
- Python 3
- `pandas`
- `numpy`

Both libraries are preinstalled in Google Colab.
