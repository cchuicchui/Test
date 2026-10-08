# Phase 4 — Consumer Workflow

[← Phase 3](phase-3-producer-workflow.md) | [Next: Phase 5 →](phase-5-talking-points.md)

---

Switch to the **Consumer** persona (second browser profile / incognito window) for all steps in this phase.

---

## Steps

### Step 12: Browse the Marketplace

1. Log in as the **Consumer** persona
2. On the DPH home page, click **Browse marketplace**
3. Use the **search bar** to find `Customer Sales Analytics`
4. Point out the search and filter capabilities to your audience:
   - Filter by **Domain** (e.g., Sales, Finance, Operations)
   - Filter by **Tags** (e.g., `quarterly`, `lakehouse`)
   - Filter by **Asset type**

> **Demo talking point:** Consumers can self-serve — no need to email a data team or raise a ticket.

---

### Step 13: Inspect the Data Product

1. Click the **Customer Sales Analytics Q3 2025** product card
2. Walk through each section:

   | Section | What to Show |
   |---|---|
   | **Overview** | Name, description, producer name, domain, `lakehouse` tag |
   | **Assets** | Schema preview from watsonx.data — column names, data types, sample rows sourced live from the Presto engine |
   | **Data contract** | Quality rules (null checks, field constraints) and SLA |
   | **Delivery options** | Data Extract (CSV/Parquet), Access in watsonx.data |

> **Demo talking point:** The data is not a stale copy — it is sourced live from the enterprise lakehouse. The contract tab gives consumers confidence in data quality *before* they subscribe.

---

### Step 14: Subscribe and Request Access

1. Click **Subscribe**
2. Fill in the **Use case** field:
   > _"Building a Q3 regional performance dashboard for the sales leadership team."_
3. Click **Submit**

#### Approve the subscription (Producer persona)

1. Switch to the **Producer** browser profile
2. Go to **My Products** → select the published product → **Subscriptions** tab
3. Find the pending request → click **Approve**
4. Switch back to the **Consumer** browser profile

---

### Step 15: Consume the Data

The consumer can now access the data product. Show one or more of the following delivery methods:

---

#### Option A — Data Extract (business user path)

1. Go to **My Subscriptions** → select **Customer Sales Analytics Q3 2025**
2. Click **Get data** → **Download as CSV** (or Parquet)
3. Open the downloaded file to confirm the data is correct

> **Demo talking point:** A business analyst can go from discovery to data in minutes, with no engineering involvement.

---

#### Option B — Access in watsonx.data (technical user path) ✨ New with this bundle

This delivery method lets consumers directly access the data product as a resource **inside watsonx.data** — no data movement required.

1. Go to **My Subscriptions** → select **Customer Sales Analytics Q3 2025**
2. Click **Get data** → **Access in watsonx.data**
3. DPH will display the **watsonx.data connection details** and the specific catalog/schema/table that has been shared
4. Open the **watsonx.data console** → go to **Query workspace**
5. Run a query against the shared table:

   ```sql
   SELECT region, product_line, SUM(revenue) AS total_revenue
   FROM <shared_catalog>.<schema>.<table>
   GROUP BY region, product_line
   ORDER BY total_revenue DESC
   ```

> **Demo talking point:** The consumer gets governed access to live lakehouse data — no file download, no data copy. The producer controls exactly what is shared, and access can be revoked at any time.

---

#### Option C — Deliver as a Table in watsonx.data (optional advanced path)

Use this to show a consumer landing a data product as a **new Iceberg table** in their own watsonx.data catalog:

1. Go to **My Subscriptions** → select the product
2. Click **Get data** → **Deliver as a table in watsonx.data**
3. Specify:
   - **Target catalog**: select an Iceberg catalog the consumer has write access to
   - **Target schema**: an existing schema or create a new one
   - **Table name**: e.g., `sales_q3_2025_delivered`
4. Click **Deliver**
5. Once complete, open the watsonx.data console → confirm the new table exists

> **Demo talking point:** The consumer can materialise the data product as a queryable table in their own lakehouse namespace — ready for BI tools, notebooks, or pipelines.

---

#### Option D — Flight Service (data scientist path, optional)

1. Open a **Jupyter Notebook** in Watson Studio (if available)
2. Use the generated Flight code snippet to access the data programmatically:

   ```python
   import ibm_watson_studio_lib as wslib

   wslib_obj = wslib.access_project_or_space({"token": "YOUR_TOKEN"})

   # Flight client connects to the data product asset directly
   # No need to know the underlying storage location or credentials
   ```

---

## Verification Checklist

- [ ] Consumer finds the published product in the Marketplace
- [ ] All product sections (overview, assets, contract, delivery) are visible
- [ ] Subscription request submitted and approved by the Producer
- [ ] Consumer downloads data via Data Extract (CSV) ✅
- [ ] Consumer accesses data via Access in watsonx.data ✅

---

[← Phase 3](phase-3-producer-workflow.md) | [Next: Phase 5 →](phase-5-talking-points.md)
