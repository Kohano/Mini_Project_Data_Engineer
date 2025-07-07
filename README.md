# Mini_Project_Data_Engineer
Praktikum
Objective:
Show that you can handle a basic ETL process:
-Extract data from a CSV
-Transform it (clean, check, add useful fields)
-Load it into a SQL database
-Run simple SQL queries for analysis
Do this in one Jupyter Notebook using only free tools — your local 
Jupyter Notebook, JupyterLite, or any other cloud-agnostic option.
🚀 Dataset
Use this small sample retail sales CSV (about 1,000
rows):
👉 Download CSV
Columns:
-date: date of sale (YYYY-MM-DD)
-product: product name
-category: product category
-price: unit price in USD
-quantity: number of units sold
-revenue: total sale revenue (should be price * quantity)
🚀 🚀 Tools
✅ Use Python 3.x
✅ Use SQLite (built into Python) for the database — no servers, no setup
✅ pandas is optional — recommended for easier CSV work
✅ Cloud-agnostic: Works with local Jupyter Notebook, JupyterLite, or any
free hosted option that supports standard Python.

✅ What You Need to Do
1) Extract
-Download the CSV file (either manually or with a simple Python 
download command).
-Place it in your working directory so your notebook can read it.
2) Transform
-Load the CSV data:
oUse pandas (pd.read_csv()) if you want — it makes CSV 
reading and type conversion easier.
oIf you don’t want pandas, use Python’s csv module.
-Check for missing or invalid data.
-Make sure numeric fields (price, quantity, revenue) are numeric.
-Add a new column: quarter (Q1–Q4) based on the date.
-Optionally verify that revenue = price * quantity.
3) Load
-Create a new SQLite database file (sqlite3.connect()).
-Create a sales_data table with the right columns.
-Load the transformed data into this table.
oIf using pandas, use DataFrame.to_sql().
oIf not using pandas, use cursor.executemany() with prepared 
statements.
-Check that the data is there (e.g., SELECT COUNT(*)).
4) Analyze
Write 6 SQL queries to answer:
1. Total revenue for all sales.
2. Total quantity sold.
3. Average product price.
4. Product with the highest total revenue.
5. Category with the highest total revenue.
6. Total revenue for each quarter (Q1–Q4).
Run each query, show the results, and briefly note your finding.
🚀 Helpful Hints
✔️  Use standard ANSI SQL.
✔️  Keep your code clear — headings for each part.
✔️  Add short markdown notes to explain what’s happening.
✔️  If you use pandas:
-It’s fine to do CSV and SQLite both with pandas (read_csv, to_sql).
-Use read_sql_query() to run SQL and see results in DataFrames.
✔️  If you don’t use pandas:
-Use Python’s sqlite3 and csv modules only.
-Loop through your data carefully, convert types where needed.
🚀 Deliverable
Submit ONE notebook (.ipynb) that:
-Runs end-to-end (restart & run all to test!)
-Has the CSV reading, cleaning, loading, and SQL queries
-Shows your query results
-Includes clear markdown explanations

