# Real Estate Market Analysis

## Background 

The real estate market is a complex and dynamic entity of great interest for professionals in the field, investors, policymakers, and data analysts that wish to thoroughly understand the market conditions and customer behavior and make informed decisions. In our Real Estate Market Analysis with Python project, the client—a leading company in the industry—has collected data on properties and their customers and wishes you to help them with the real estate analysis. 

## Project Objective

This Real Estate Market Analysis with Python project aims to preprocess, analyze, and visualize the real estate property data, thereby generating meaningful insights about property transactions and customer profiles. The main analysis is contained in [`real_estate_market_analysis.ipynb`](real_estate_market_analysis.ipynb).

## Project Overview

The notebook combines customer and property data to investigate:

- Property sales by building and year
- Average area, price, and deal satisfaction by building
- Sales distribution by country and state
- Sales across customer age intervals
- The relationship between customer age and property price for sold properties purchased by individuals

The project is designed as a practical data-cleaning and exploratory-analysis exercise using pandas, NumPy, Matplotlib, and Seaborn.

## Data

The project uses two CSV files:

- [`customers.csv`](customers.csv): comprises customer details, such as customer ID, entity, name, surname, and more.
- [`properties.csv`](properties.csv): contains details about the properties, including ID, building details, sale date, etc.

## Analysis Workflow

`real_estate_market_analysis.ipynb` follows this general workflow:

1. Import the analysis libraries.
2. Load data files.
3. Data cleaning and preprocessing
4. Merge property records with customer records using `customerid`.
5. Produce descriptive statistics and grouped summaries.
6. Visualize sales, pricing, customer age, and geographic patterns.

## Main Outputs

The notebook produces:

- Building-level totals and annual sales tables
- Annual sales bar charts
- Cumulative sales trend charts
- Building-level comparisons of average area, price, and deal satisfaction
- Country-level descriptive statistics
- US state sales frequency and cumulative-frequency analysis
- Sales distribution by customer age interval
- Sold and unsold property counts by price interval
- A scatter plot and correlation measure for customer age versus property price

## Setup

Create and activate a virtual environment from the project directory:

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

Install the required packages:

```powershell
python -m pip install pandas numpy matplotlib seaborn jupyter
```

## Run the Notebook

Start Jupyter from the project directory so the relative CSV paths resolve correctly:

```powershell
jupyter notebook
```

Open `real_estate_market_analysis.ipynb`, restart the kernel, and run all cells from top to bottom. The notebook expects `customers.csv` and `properties.csv` to remain in the same directory.

For a headless environment, configure Matplotlib to use a non-GUI backend before importing `pyplot`:

```python
import matplotlib
matplotlib.use("Agg")
import matplotlib.pyplot as plt
```

## Reproducibility Notes

- The analysis is exploratory and depends on the values and formatting present in the CSV files.
- The notebook uses relative file paths, so it should be run from the project directory.
- Re-run the notebook from a fresh kernel after changing any cleaning or transformation step.
- Missing values and text normalization should be checked before interpreting geographic and customer-level summaries.
- Validate cumulative building totals before using those charts for reporting; cumulative values should be calculated independently for each building.

