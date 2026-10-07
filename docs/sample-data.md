# Sample Data Recommendations

[← Back to README](../README.md)

---

Use any of the following free, publicly available datasets as demo data. Choose one that resonates with your target audience.

---

## Recommended Datasets

### Option 1: Sales Data (general audience)

A simple synthetic sales CSV works well for most audiences.

**Suggested schema:**

```csv
region,product_category,quarter,revenue,units_sold,sales_rep
North,Electronics,Q3 2025,142500,320,Alice Johnson
South,Furniture,Q3 2025,98700,210,Bob Smith
East,Electronics,Q3 2025,175000,400,Carol White
West,Apparel,Q3 2025,63200,530,David Lee
```

Create a file named `sales_q3_2025.csv` with 20–50 rows for a realistic preview.

---

### Option 2: NYC Taxi Trip Data (public dataset)

- **Source:** [NYC TLC Trip Record Data](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page)
- **Format:** CSV / Parquet
- **Best for:** Technology and data engineering audiences
- **Tip:** Download a single month and trim to ~1,000 rows to keep the demo fast

---

### Option 3: Weather Data (NOAA)

- **Source:** [NOAA Climate Data Online](https://www.ncdc.noaa.gov/cdo-web/)
- **Format:** CSV
- **Best for:** Audiences in utilities, agriculture, insurance, or logistics

---

### Option 4: World Bank Open Data

- **Source:** [data.worldbank.org](https://data.worldbank.org)
- **Format:** CSV / Excel
- **Best for:** Government, NGO, or financial services audiences

---

## Tips for Preparing Demo Data

- **Trim the dataset** to 50–200 rows — large files slow down the UI preview
- **Clean column names** — use `snake_case` or `PascalCase` (avoid spaces in column headers)
- **Add a mix of data types** — include at least one numeric column, one string column, and one date column to make the schema preview more interesting
- **Include a deliberately suspicious row** (e.g., a null revenue value) if you plan to demonstrate data contract quality rules catching issues

---

## File Naming Convention

```
<domain>_<dataset_name>_<period>.csv

Examples:
  sales_regional_q3_2025.csv
  weather_chicago_jan_2025.csv
  customers_us_2025.csv
```

---

[← Back to README](../README.md)
