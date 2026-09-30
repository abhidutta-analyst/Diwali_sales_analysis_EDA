# Diwali Sales Analysis

An exploratory analysis of retail transactions during the Diwali sales period. This project uses Python to clean the supplied transaction-level dataset, profile customer and product patterns, and visualize sales amount and order volume across key segments.

## Project Overview

The analysis is delivered as an executable Jupyter notebook. It moves from data quality checks and preparation into exploratory analysis, aggregation, and chart-based comparison. The goal is to surface useful patterns in the available records, not to infer customer behavior beyond what these data support.

## Key Findings

The notebook's grouped comparisons indicate the following patterns in this dataset:

- **Gender:** Female customers account for more records and a higher summed sales amount than male customers.
- **Age:** The 26–35 age band is the largest segment by customer records and contributes the highest sales amount. Within this band, female customers are the most represented group.
- **Geography:** Uttar Pradesh, Maharashtra, and Karnataka rank among the leading states for both order volume and sales amount.
- **Marital status:** The group coded as married contributes more records and sales amount; the gender split shows married women as the largest contributing segment.
- **Occupation:** Customers associated with IT, Healthcare, and Aviation appear among the leading occupations by sales amount.
- **Product mix:** Food, Clothing, and Electronics are the leading categories highlighted by the notebook's sales and order comparisons.

These are descriptive findings from the available dataset. They do not establish that demographic or occupational attributes cause higher purchasing, and the source contains no time-series field with which to measure a seasonal uplift against a baseline.

## Dataset and Preparation

The source file, `Diwali Sales Data.csv`, contains 11,251 rows and 15 columns before cleaning. The notebook removes two entirely empty export columns (`Status` and `unnamed1`), drops 12 records missing `Amount`, and converts `Amount` to an integer. The resulting analysis frame contains 11,239 rows and 13 columns.

Fields used include customer and product identifiers, gender, age and age group, marital-status code, state, zone, occupation, product category, order count, and amount. The dataset does not define a currency unit in the notebook, so this README refers to values as sales amount rather than assigning a currency.

## Analysis Workflow

1. Load the CSV into a pandas DataFrame.
2. Inspect dimensions, sample rows, column types, and missing values.
3. Remove empty columns and records without a sales amount; convert amount values to integers.
4. Use descriptive statistics and grouped aggregations to compare customer records, order counts, and summed sales amounts.
5. Visualize patterns across gender, age group, state, marital status, occupation, product category, and product ID.
6. Summarize the strongest observed patterns and their limitations.

## Tools

- Python
- Jupyter Notebook
- pandas and NumPy for data handling
- Matplotlib and Seaborn for visualization

## Run the Notebook

1. Clone or download this repository and open a terminal in the project directory.
2. Install the dependencies:

   ```bash
   python -m pip install pandas numpy matplotlib seaborn jupyter
   ```

3. Start Jupyter:

   ```bash
   jupyter notebook
   ```

4. Open `Diwali_Sales_Analysis.ipynb` and run the cells from top to bottom. Keep `Diwali Sales Data.csv` in the same directory as the notebook.

## Repository Contents

- `Diwali_Sales_Analysis.ipynb` — data cleaning, exploratory analysis, visualizations, and written conclusions.
- `Diwali Sales Data.csv` — source transaction dataset used by the notebook.

## Limitations and Next Steps

The notebook is exploratory and works from a single supplied dataset. The findings are descriptive, not causal; order counts represent recorded orders in the source rather than necessarily unique customers. The data dictionary and currency are not included, and the analysis does not test statistical significance or compare Diwali-period performance with other periods.

Potential next steps include validating category and demographic definitions with a data dictionary, checking whether customer IDs represent unique people consistently, adding a time dimension and comparison period, and building a reproducible report with documented dependency versions.

## Acknowledgment

This project uses the Diwali sales dataset provided with the repository. Dataset attribution and licensing should be confirmed from the original source before redistribution.
