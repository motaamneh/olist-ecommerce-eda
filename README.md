# Olist E-commerce EDA

Exploratory data analysis of the Olist Brazilian e-commerce dataset using pandas. The notebook answers five business questions, with a chart and a one-sentence insight for each, and includes two questions redone in SQL.

## Project structure

```
.
├── Data/             Olist CSV files (source data)
├── src/              Helper scripts
├── outputs/          Saved charts and the findings note
├── EDA.ipynb         Main analysis notebook
├── requirements.txt  Pinned Python dependencies
└── README.md
```

## Dataset

[Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) (Kaggle). The CSVs are included in `Data/`. If they are missing, download the dataset from Kaggle and extract the files into `Data/`.

## Tools used

| Tool | Purpose |
|---|---|
| Python 3.12 | Language (tested on 3.12.10) |
| pandas, numpy | Loading, filtering, grouping and joining the tables |
| scipy | Outlier checks (z-score, IQR) |
| matplotlib, seaborn | Charts |
| sqlite3 (built into Python) | SQL queries (SELECT, WHERE, GROUP BY, JOIN) |
| Jupyter Notebook | Running `EDA.ipynb` |
| nbconvert, nbformat | Re-running the notebook from the command line |

Exact versions are pinned in `requirements.txt`.

## Setup

1. Install Python 3.12 and Git.

2. Clone the repository:
   ```
   git clone https://github.com/motaamneh/olist-ecommerce-eda.git
   cd olist-ecommerce-eda
   ```

3. Create and activate a virtual environment:

   Windows (PowerShell):
   ```
   python -m venv venv
   venv\Scripts\Activate.ps1
   ```
   macOS / Linux:
   ```
   python3 -m venv venv
   source venv/bin/activate
   ```

4. Install the dependencies:
   ```
   pip install -r requirements.txt
   ```

5. Open the notebook:
   ```
   jupyter notebook EDA.ipynb
   ```
   In VS Code, open `EDA.ipynb` and select the `venv` interpreter as the kernel.

## Re-running the notebook

To run the whole notebook top to bottom without errors:

```
jupyter nbconvert --to notebook --execute EDA.ipynb --output EDA.ipynb
```

## Notes

- `venv/` is not committed. Recreate it with the steps above.
- If PowerShell blocks the activation script, run `Set-ExecutionPolicy -Scope CurrentUser RemoteSigned` once and try again.
