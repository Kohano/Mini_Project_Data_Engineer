# Mini Data Engineering Project: ETL with SQLite

🧪 Praktikum (Practical Exercise)
🎯 Objective
This project demonstrates a basic ETL (Extract, Transform, Load) pipeline using only free and lightweight tools.

You will:

✅ Extract data from a CSV file

✅ Transform the data (clean, validate, enrich)

✅ Load the data into a SQLite database

✅ Analyze the data with simple SQL queries

Everything is done in a single Jupyter Notebook, with no external servers or cloud dependencies.


#📦Dataset
We’re using a sample retail sales dataset with around 1,000 rows. Each row represents a product sale and contains:
| Column     | Description                      |
| ---------- | -------------------------------- |
| `date`     | Date of sale (YYYY-MM-DD)        |
| `product`  | Name of the product sold         |
| `category` | Product category                 |
| `price`    | Unit price in USD                |
| `quantity` | Number of units sold             |
| `revenue`  | Total revenue = price × quantity |


#Tools & Requirements
✅ Python 3.x

✅ SQLite (built into Python via the sqlite3 module)

✅ Jupyter Notebook (local or cloud-agnostic, e.g. JupyterLite)

✅ Optional: pandas (recommended for easier CSV and SQL handling)


#🧪 What You’ll Do
1️⃣ Extract
Load the CSV file using either:

pandas.read_csv(), or

Python’s built-in csv module

Ensure it’s in your local directory for the notebook to read.

2️⃣ Transform
Clean and validate the data:

Check for missing or invalid fields

Ensure numeric columns (price, quantity, revenue) are correctly typed

Optionally verify that revenue = price × quantity

Add a new column:

quarter (Q1–Q4) based on the date field

3️⃣ Load
Create a SQLite database file using sqlite3.connect()

Define a table sales_data with appropriate columns

Load the cleaned data:

Use DataFrame.to_sql() if using pandas

Or cursor.executemany() with SQL statements if not

Verify the load (e.g., using SELECT COUNT(*))

4️⃣ Analyze
Run these 6 SQL queries on the loaded data:

🔢 Total revenue for all sales

🔢 Total quantity sold

💲 Average product price

🥇 Product with the highest total revenue

🏆 Category with the highest total revenue

🗓 Total revenue for each quarter (Q1–Q4)


#💡 Tips
Use standard SQL (ANSI SQL)

Keep your code well-organized using sections and markdown cells

Use pandas.read_sql_query() if you're working with pandas to view SQL results as DataFrames

If not using pandas, handle data type conversions carefully with built-in Python modules


#Deliverable
You will submit one Jupyter Notebook (.ipynb) that:

Runs end-to-end (Restart and Run All should work)

Includes all steps: CSV loading, cleaning, transformation, SQLite loading, and SQL querying

Displays query results clearly

Includes markdown explanations throughout
