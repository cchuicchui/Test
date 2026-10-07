# Phase 4 — Consumer Workflow

[← Phase 3](phase-3-producer-workflow.md) | [Next: Phase 5 →](phase-5-talking-points.md)

---

Switch to the **Consumer** persona (second browser profile / incognito window) for all steps in this phase.

---

## Steps

### Step 10: Browse the Marketplace

1. Log in as the **Consumer** persona
2. On the DPH home page, click **Browse marketplace**
3. Use the **search bar** to find `Customer Sales Analytics`
4. Point out the search and filter capabilities to your audience:
   - Filter by **Domain** (e.g., Sales, Finance, Operations)
   - Filter by **Tags** (e.g., `quarterly`, `analytics`)
   - Filter by **Asset type**

> **Demo talking point:** Consumers can self-serve — no need to email a data team or raise a ticket.

---

### Step 11: Inspect the Data Product

1. Click the **Customer Sales Analytics Q3 2025** product card
2. Walk through each section:

   | Section | What to Show |
   |---|---|
   | **Overview** | Name, description, producer name, domain |
   | **Assets** | Schema preview — column names, data types, sample rows |
   | **Data contract** | Quality rules and SLA (if defined in Phase 3, Step 8) |
   | **Delivery options** | Available access methods (CSV extract, Flight service) |

> **Demo talking point:** The contract tab gives consumers confidence in data quality **before** they subscribe.

---

### Step 12: Subscribe and Request Access

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

### Step 13: Consume the Data

The consumer can now access the data product. Show one or both delivery methods:

#### Option A — Data Extract (business user path)

1. Go to **My Subscriptions** → select **Customer Sales Analytics Q3 2025**
2. Click **Get data** → **Download as CSV** (or Parquet)
3. Open the downloaded file to confirm the data is correct

> **Demo talking point:** A business analyst can go from discovery to data in minutes, with no engineering involvement.

#### Option B — Flight Service (technical user path, optional)

1. Open a **Jupyter Notebook** in Watson Studio (if available in your environment)
2. Use the generated Flight code snippet to access the data programmatically:

   ```python
   import ibm_watson_studio_lib as wslib

   wslib_obj = wslib.access_project_or_space({"token": "YOUR_TOKEN"})

   # The Flight client connects to the data product asset directly
   # No need to know the underlying storage location or credentials
   ```

> **Demo talking point:** Data scientists get direct programmatic access — same product, different delivery format for different user types.

---

## Verification Checklist

- [ ] Consumer can find the published product in the Marketplace
- [ ] All product sections (overview, assets, contract, delivery) are visible
- [ ] Subscription request submitted successfully
- [ ] Producer approved the subscription
- [ ] Consumer downloaded the data (CSV extract) successfully

---

[← Phase 3](phase-3-producer-workflow.md) | [Next: Phase 5 →](phase-5-talking-points.md)
