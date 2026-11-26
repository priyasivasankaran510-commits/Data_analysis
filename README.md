# Data_analysis
# Synthetic Sales Analysis Notebook (Milestone 3)

A Jupyter/Colab data analysis project inspecting a synthetic sales dataset (`sales.csv` and `sales-dirty.csv`) using Python, pandas, and Matplotlib[cite: 2, 3].

## Project Overview

This notebook completes **Milestone 3** of the **EdBytes Data Analytics Virtual Internship**[cite: 1, 2, 3]. It covers data loading, missing-value and duplicate handling, revenue metric calculations, category-level visualization, and edge-case testing[cite: 3].

## Files in This Repository

* `analysis.ipynb` — Main Jupyter/Colab notebook with executed code cells and regenerated outputs[cite: 2, 3].
* `sales.csv` — Clean synthetic dataset containing 8 fictional sales orders (`OrderID`, `Date`, `Region`, `Category`, `Quantity`, `UnitPrice`)[cite: 3].
* `sales-dirty.csv` — Uncleaned version of the dataset (10 rows) containing a blank row and a duplicate `OrderID` (`S03`) used to practice data cleaning[cite: 3].
* `.gitattributes` — Configures line endings and marks Jupyter Notebook diffs cleanly on GitHub.

## Key Steps & Findings

1. **Data Inspection & Cleaning:** Verified `sales.csv` (8 rows, 6 columns) has `0` missing values[cite: 3]. Cleaned `sales-dirty.csv` by dropping completely empty rows (`dropna(how='all')`) and deduplicating `OrderID` (`keep='first'`), restoring the exact 8-row structure[cite: 3].
2. **Revenue Metrics:**
   * **Total Orders:** 8[cite: 3]
   * **Total Revenue:** 4,700[cite: 3]
   * **Average Order Value (AOV):** 587.5[cite: 3]
3. **Category Breakdown:**
   * **Bags:** 3,200 revenue (68.1% share, 4 units across 3 orders)[cite: 3]
   * **Books:** 1,200 revenue (25.5% share, 6 units across 3 orders)[cite: 3]
   * **Pens:** 300 revenue (6.4% share, 15 units across 2 orders)[cite: 3]
4. **Edge-Case Testing:** Built `summarize_safe()` to handle empty DataFrames gracefully by returning `0` instead of `NaN` for average order value when order count is zero[cite: 3].

## How to Run

1. Open the `.ipynb` file in **Google Colab** or **Jupyter Notebook**[cite: 2, 3].
2. Place `sales.csv` and `sales-dirty.csv` in the same working directory (in Colab: **Files → Upload**)[cite: 3].
3. Run all cells from top to bottom (**Runtime → Run all**)[cite: 3].
