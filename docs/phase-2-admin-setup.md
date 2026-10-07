# Phase 2 — Initial Setup (Admin Role)

[← Phase 1](phase-1-techzone-setup.md) | [Next: Phase 3 →](phase-3-producer-workflow.md)

---

## Steps

### Step 2: Access DPH and Verify the Environment

1. Open the URL from your TechZone confirmation email
2. Log in with the provided credentials (or your IBM Cloud ID if using the SaaS path)
3. Confirm you are in the **Data Product Hub** experience:
   - The top navigation should read **"Data Product Hub"**
   - The home page shows cards for **Create a data product** and **Browse marketplace**
4. Navigate to **Administration** and verify the following services are active:

   | Service | Expected Status |
   |---|---|
   | Data Product Hub | ✅ Active |
   | Object Storage | ✅ Active (required for data extracts) |

---

### Step 3: Create User Personas

For a realistic demo, you need two personas — a **Producer** and a **Consumer**. This makes the demo storytelling much clearer for your audience.

#### Option A: Create separate user accounts (preferred)

1. Go to **Administration** → **Users** → **Add user**
2. Create the following users:

   | Display Name | Email | Role |
   |---|---|---|
   | `Demo Producer` | `producer@demo.com` | Data Engineer or Editor |
   | `Demo Consumer` | `consumer@demo.com` | Viewer |

3. Set temporary passwords and note them down

#### Option B: Use browser profiles (if user creation is restricted)

If you only have one admin account, simulate two personas using separate browser profiles:

- **Chrome Profile 1** → Producer (your admin account)
- **Chrome Profile 2 / Incognito** → Consumer (same or a second account)

---

## Verification Checklist

Before moving to Phase 3, confirm the following:

- [ ] DPH home page is accessible and shows the correct experience
- [ ] Administration panel is accessible
- [ ] At least two user personas are available (or browser profiles are set up)
- [ ] Object Storage service is active

---

[← Phase 1](phase-1-techzone-setup.md) | [Next: Phase 3 →](phase-3-producer-workflow.md)
