# Phase 3 — Producer Workflow

[← Phase 2](phase-2-admin-setup.md) | [Next: Phase 4 →](phase-4-consumer-workflow.md)

---

Log in as the **Producer** persona for all steps in this phase.

---

## Steps

### Step 5: Create a Project

1. From the DPH home page, go to **Projects** → **New Project**
2. Name the project: `Demo Data Project`
3. Click **Create**

---

### Step 6: Create a Connection Asset to watsonx.data

The DPH Initialization bundle pre-creates a Presto connection. Add it to your project:

1. Inside `Demo Data Project`, click **Assets** → **New Asset** → **Connection**
2. Select **IBM watsonx.data (Presto)** from the connection type list
3. If a pre-existing connection is available, select it. Otherwise fill in the details:

   | Field | Value |
   |---|---|
   | **Connection name** | `watsonx.data Demo Connection` |
   | **Hostname** | From watsonx.data console → Connection information |
   | **Port** | `443` |
   | **Authentication** | Username + API key (from IBM Cloud) |

4. Click **Test connection** → confirm success → **Create**

---

### Step 7: Create a Data Product

1. From the home page, click **Create a data product**
2. Fill in the product details:

   | Field | Example Value |
   |---|---|
   | **Name** | `Customer Sales Analytics Q3 2025` |
   | **Description** | `Quarterly sales data aggregated by region and product category, sourced directly from the enterprise lakehouse and curated for BI teams.` |
   | **Domain** | `Sales` |
   | **Tags** | `sales`, `quarterly`, `analytics`, `lakehouse` |
   | **Status** | `Draft` (default) |

3. Click **Next**

---

### Step 8: Add a Data Asset from watsonx.data

#### Option A: Add a table directly from watsonx.data (recommended)

1. Click **Add asset** → **Data asset from source**
2. Select the **watsonx.data (Presto) connection** created in Step 6
3. Browse the catalog and schema to locate a suitable table (e.g., `gosales.go_daily_sales` or any pre-loaded table noted in Phase 2)
4. Select the table → click **Add**
5. Preview the data — confirm the schema columns are visible
6. Click **Next**

#### Option B: Add a parameterized SQL query asset

Use this to show dynamic, consumer-driven filtering of lakehouse data:

1. Click **Add asset** → **SQL query asset**
2. Select the **watsonx.data (Presto) connection**
3. Enter a parameterized query, for example:

   ```sql
   SELECT region, product_line, SUM(revenue) AS total_revenue, COUNT(*) AS order_count
   FROM gosales.go_daily_sales
   WHERE year = {{ year }}
   GROUP BY region, product_line
   ORDER BY total_revenue DESC
   ```

4. Define the parameter:
   - **Name**: `year`
   - **Type**: String
   - **Default value**: `2024`
5. Click **Save** → **Add**

> **Demo talking point:** The producer packages a reusable query. Consumers can run it with different parameters without ever touching the underlying lakehouse directly.

---

### Step 9: Define Delivery Methods

Select the delivery options consumers will have:

| Delivery Method | Best For | Select for Demo |
|---|---|---|
| **Data Extract (CSV/Parquet)** | Business users who download files | ✅ Yes |
| **Access in watsonx.data** | Technical users who query directly in watsonx.data | ✅ Yes |
| **Deliver as a Table in watsonx.data** | Consumers who want the data landed as a new table | Optional |
| **Flight service** | Data scientists using Jupyter Notebooks | Optional |

Enable at least **Data Extract** and **Access in watsonx.data** for a complete demo.

---

### Step 10: Define a Data Contract

A data contract is a formal producer/consumer agreement that builds trust in the data product.

1. Click the **Contract** tab → **Add contract**
2. Define the contract properties:

   | Property | Example Value |
   |---|---|
   | **Schema** | Confirm expected columns from the watsonx.data table |
   | **Quality rule** | `revenue` column must not be null |
   | **Quality rule** | `region` must not be empty |
   | **SLA / Refresh** | Daily (sourced live from lakehouse) |

3. Save the contract

> The contract shows up as a **trust indicator badge** on the marketplace listing and is enforced via the watsonx.data intelligence data quality engine.

---

### Step 11: Publish the Data Product

1. Review all tabs:
   - **Details** — name, description, domain, tags
   - **Assets** — watsonx.data table or SQL query preview
   - **Delivery** — delivery methods enabled
   - **Contract** — quality rules and SLA
2. Click **Publish** → confirm the dialog
3. Verify the status changes from `Draft` → `Published`
4. The product is now visible in the **Marketplace**

---

## Verification Checklist

- [ ] Project created with a watsonx.data Presto connection
- [ ] Data product created with name, description, domain, and tags
- [ ] A watsonx.data table or SQL query asset added with visible schema
- [ ] Data Extract and Access in watsonx.data delivery methods enabled
- [ ] Data contract defined with at least one quality rule
- [ ] Product status is `Published` and appears in the Marketplace

---

[← Phase 2](phase-2-admin-setup.md) | [Next: Phase 4 →](phase-4-consumer-workflow.md)
