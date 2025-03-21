# Home Sales Analysis with SparkSQL

## Project Files
- `home_Sales.ipynb`: Jupyter notebook containing SparkSQL analysis.
- Dataset source: AWS S3 bucket (`home_sales_revised.csv`).

## Key Tasks Performed

- **Data Importing:** Loaded the dataset into a Spark DataFrame.
- **Temporary Tables:** Created and managed temporary views.
- **SparkSQL Queries:**
  - Calculated average home prices for specific criteria:
    - Four-bedroom houses per sale year.
    - Three-bedroom, three-bathroom homes per year built.
    - Three-bedroom, three-bathroom, two-floor homes over 2,000 sqft per year built.
    - Average home price per "view" rating, filtering by homes priced ≥ $350,000.
- **Performance Optimization:**
  - Cached and validated temporary tables.
  - Compared query performance (cached vs. uncached).
  - Partitioned the dataset by `date_built` and stored it in Parquet format for enhanced query efficiency.
- **Table Uncaching:** Verified uncaching of temporary tables.
