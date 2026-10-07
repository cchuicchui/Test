# Phase 3 — Producer Workflow

[← Phase 2](phase-2-admin-setup.md) | [Next: Phase 4 →](phase-4-consumer-workflow.md)

---

Log in as the **Producer** persona for all steps in this phase.

---

## Steps

### Step 4: Upload Sample Data

1. From the DPH home page, go to **Projects** → **New Project**
2. Name the project: `Demo Data Project`
3. Click **Assets** → **New Asset** → **Data** → **Load**
4. Upload your sample CSV file

> See [sample-data.md](sample-data.md) for recommended free datasets.

---

### Step 5: Create a Data Product

1. From the home page, click **Create a data product**
2. Fill in the product details:

   | Field | Example Value |
   |---|---|
   | **Name** | `Customer Sales Analytics Q3 2025` |
   | **Description** | `Quarterly sales data aggregated by region and product category, curated for BI teams.` |
   | **Domain** | `Sales` |
   | **Tags** | `sales`, `quarterly`, `analytics` |
   | **Status** | `Draft` (default) |

3. Click **Next**

---

### Step 6: Add a Data Asset

1. Click **Add asset** → **Data asset from project**
2. Select the CSV uploaded in Step 4
3. Preview the data — confirm the schema columns are visible
4. Click **Next**

#### Optional: Add a parameterized SQL query asset

Instead of (or in addition to) the CSV, add a SQL query to show dynamic filtering:

```sql
SELECT region, product_category, SUM(revenue) AS total_revenue
FROM sales_data
WHERE quarter = '{{ quarter }}'
GROUP BY region, product_category
```

This demonstrates how consumers can request filtered data without moving raw datasets.

---

### Step 7: Define Delivery Methods

Select the delivery options consumers will have when they access this product:

| Delivery Method | Best For | Select for Demo |
|---|---|---|
| **Data Extract (CSV/Parquet)** | Business users who download files | ✅ Yes (required) |
| **Flight service** | Technical users (data scientists, notebooks) | Optional |

Enable at least **Data Extract** for the simplest demo path.

---

### Step 8: Define a Data Contract *(optional but recommended)*

A data contract is a formal producer/consumer agreement. Including it in the demo builds the trust and governance story.

1. Click the **Contract** tab → **Add contract**
2. Define the contract properties:

   | Property | Example Value |
   |---|---|
   | **Schema** | Confirm expected columns: `region`, `revenue`, `quarter`, `product_category` |
   | **Quality rule** | `revenue` column must not be null |
   | **Quality rule** | `region` must be one of: `North`, `South`, `East`, `West` |
   | **SLA / Refresh** | Quarterly |

3. Save the contract

> The contract shows up as a **trust indicator badge** on the marketplace listing.

---

### Step 9: Publish the Data Product

1. Review all tabs:
   - **Details** — name, description, domain, tags
   - **Assets** — data preview, schema
   - **Delivery** — delivery methods enabled
   - **Contract** — quality rules and SLA
2. Click **Publish** → confirm the dialog
3. Verify the status changes from `Draft` → `Published`
4. The product is now visible in the **Marketplace**

---

## Verification Checklist

- [ ] Sample CSV uploaded to the project
- [ ] Data product created with name, description, domain, and tags
- [ ] At least one data asset added with visible schema
- [ ] Data Extract delivery method enabled
- [ ] Data contract defined (optional but recommended)
- [ ] Product status is `Published`
- [ ] Product appears in the Marketplace

---

[← Phase 2](phase-2-admin-setup.md) | [Next: Phase 4 →](phase-4-consumer-workflow.md)
