# building-expense-analysis
Python project for analyzing one year of residential building expenses, with per-unit cost distribution logic, categorized spending trends, and clear visualizations. Cleaned dataset, full analysis, and export-ready visual assets included.

# 📊 Building Expense Analysis (1-Year)

## Overview

This project analyzes one year of operational expenses for a residential building, focusing on fair cost attribution across individual units. It includes data cleaning, categorization, aggregation, and multiple visualizations.

## Objectives

* Understand total and per-category building expenses
* Attribute cost shares to 11 units based on usage rules
* Identify cost trends and seasonal patterns
* Visualize insights for stakeholders or portfolio display

## Dataset

**File**: `building.xlsx`
**Structure**:

* `Month`: Month of expense
* `Cost`: Description of the cost
* `Amount`: Cost in Toman
* `Date`: Date of transaction (not used in analysis)
* `Units involve`: Either "All" or "But 1,3"

## Data Preparation

* Removed rows with missing values
* Converted `Amount` from string to integer
* Normalized cost names and fixed typos
* Grouped similar costs into categories (e.g. Plumbing, Cleaning)
* Parsed `Units involve` to determine cost-sharing logic:

  * "All" → shared among all 11 units
  * "But 1,3" → shared among units 2,4–11 only

## Key Features

* **Cost Category Classification** (15+ unique costs into 7 logical categories)
* **Per-Unit Cost Sharing Calculation** based on involvement
* **Pivot Tables** for trends across months and categories

## Results

### Total Paid Per Unit

* Units 1 & 3 paid less (excluded from elevator costs)
* Units 2,4–11 shared the rest equally

### Highest & Lowest Costs

* Max: Water Bill (2M+ Toman)
* Min: Cleaning (40K Toman)

### Visualizations

* Bar chart: Total paid by unit
* Pie chart: Cost distribution by category
* Line chart: Monthly cost trends
* Stacked bar chart: Frequency of costs per month

## Tools

* Python (Pandas, Matplotlib)
* Excel (initial data entry & cleanup)

## How to Use

1. Load the `building.xlsx` file
2. Run preprocessing (data cleaning, categorization, share calculation)
3. Execute visualizations
4. Review and export insights

## Repository Structure

```
.
├── building.xlsx                # Cleaned data
├── building_expense_analysis.ipynb  # Full code & analysis
├── report_visuals/           # Generated charts
├── Document of what we did   # Doc file
├── README.md                 # This file
```

## Author

Created by \[Yasaman Yaghoubi] — Data Analyst & Python Enthusiast

Feel free to fork, use, or modify for your own building or community project!
