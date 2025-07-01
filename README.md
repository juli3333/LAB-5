ETL Extract Lab

Name: Julie Koki  Muema
Student ID: 669996

LAB 3
Description
This notebook demonstrates how to perform:
- Full data extraction
- Incremental data extraction based on a timestamp

It uses a CSV dataset of sales records.

Tools Used
- Python
- pandas
- Jupyter Notebook

How to Run
1. Open `etl_extract.ipynb` in Jupyter
2. Ensure `custom_data.csv` and `last_extraction.txt` are in the same folder
3. Run all cells in the notebook

Data Source
Custom dataset (`custom_data.csv`) with realistic transaction records.

LAB 4 - Transformation in ETL

This lab extends Lab 3 by adding a transformation step to the ETL pipeline.

Transformations Implemented:
- Cleaning: Removed duplicates, handled missing values in `Quantity` and `Price`
- Enrichment: Added `TotalPrice = q\Quantity * Price`
- Structural: Converted `Date` to datetime
- Categorization: Binned `TotalPrice` into categories (Low, Medium, High, Very High)

Outputs:
- `transformed_full.csv`
- `transformed_incremental.csv`

LAB 5-Load

 This lab uses pandas and sqlite3 to load converted CSV data into a SQLite database.  

 **Created files:**
 - full_data.db/loaded_data
 - incremental_data.db/loaded_data

 Steps for Loading:
 1. Reads converted CSV files
 2. Uses SQLite to store them as tables.
 3. Verifies by looking at the first five rows.

 For the precise loading code, see `etl_load.ipynb`.