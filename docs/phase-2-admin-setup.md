# Phase 2 — Initial Setup (Admin Role)

[← Phase 1](phase-1-techzone-setup.md) | [Next: Phase 3 →](phase-3-producer-workflow.md)

---

## Steps

### Step 2: Access the Environment and Verify Services

1. Open the URL from your TechZone confirmation email
2. Log in with the provided credentials
3. Confirm you are in the **Data Product Hub** experience:
   - The top navigation should read **"Data Product Hub"**
   - The home page shows cards for **Create a data product** and **Browse marketplace**
4. Navigate to **Administration** and verify all three services are active:

   | Service | Expected Status |
   |---|---|
   | Data Product Hub | ✅ Active |
   | watsonx.data | ✅ Active |
   | watsonx.data intelligence | ✅ Active |

5. Navigate to **Administration** → **Connections** (or open the watsonx.data console) and confirm that a **Presto connection** to watsonx.data is already present. This connection is pre-created by the DPH Initialization bundle.

> If the Presto connection is missing, see [Troubleshooting: Create a Presto connection manually](#troubleshooting-create-a-presto-connection-manually) below.

---

### Step 3: Verify Sample Data in watsonx.data

The bundle may include pre-loaded sample tables in watsonx.data. Confirm this before building the data product:

1. Open the **watsonx.data** console (from the switcher or Administration)
2. Go to **Data manager** → browse the available catalogs and schemas
3. Look for pre-loaded sample tables (common examples: `gosales`, `ontime`, `tpch`, or similar)
4. If sample tables exist, note the **catalog name**, **schema name**, and **table name** — you will use these in Phase 3
5. If no sample tables exist, you can load your own — see [sample-data.md](sample-data.md)

---

### Step 4: Create User Personas

For a realistic demo you need two personas — a **Producer** and a **Consumer**.

#### Option A: Create separate user accounts (preferred)

1. Go to **Administration** → **Users** → **Add user**
2. Create the following users:

   | Display Name | Email | Role |
   |---|---|---|
   | `Demo Producer` | `producer@demo.com` | Data Engineer or Editor |
   | `Demo Consumer` | `consumer@demo.com` | Viewer |

3. Set temporary passwords and note them down

#### Option B: Use browser profiles (if user creation is restricted)

- **Chrome Profile 1** → Producer (your admin account)
- **Chrome Profile 2 / Incognito** → Consumer (same or a second account)

---

## Troubleshooting: Create a Presto Connection Manually

If the Presto connection to watsonx.data is not pre-created:

1. In DPH, go to **Projects** → open or create a project
2. Click **Assets** → **New Asset** → **Connection**
3. Select **IBM watsonx.data (Presto)**
4. Fill in the connection details from your watsonx.data instance:
   - **Hostname**: from the watsonx.data console → Connection information
   - **Port**: `443` (default)
   - **Username / API key**: from your IBM Cloud credentials
5. Click **Test connection** → confirm success → **Create**

---

## Verification Checklist

Before moving to Phase 3, confirm the following:

- [ ] DPH, watsonx.data, and watsonx.data intelligence are all active
- [ ] A Presto connection to watsonx.data exists (pre-created or manually created)
- [ ] At least one table is visible in watsonx.data Data manager
- [ ] Two user personas are available (or browser profiles are set up)

---

[← Phase 1](phase-1-techzone-setup.md) | [Next: Phase 3 →](phase-3-producer-workflow.md)
