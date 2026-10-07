# Phase 5 — Demo Talking Points

[← Phase 4](phase-4-consumer-workflow.md) | [Back to README →](../README.md)

---

Use this phase as a reference while delivering the demo to a customer or stakeholder audience.

---

## Story Arc

### The Problem (set context before the demo)

> _"Today, data consumers — analysts, data scientists, and business users — waste days or weeks trying to find data. When they do find it, they don't know if it's trustworthy, up to date, or approved for their use case. They raise tickets, send emails, and wait. Meanwhile, data engineers are buried in ad-hoc data requests instead of building pipelines."_

### The Solution (transition into the demo)

> _"IBM Data Product Hub turns data into a product — something that is curated, documented, governed, and delivered through a self-service marketplace. Let me show you how that works from both sides."_

---

## Talking Points by Demo Step

### When showing the Marketplace (Step 10)

- "This is the data marketplace — a single place where consumers can find all approved, curated data products across the organization."
- "Notice the search and filters. Consumers can filter by domain, tags, or asset type. No need to know which team owns the data."

### When showing the Data Product Detail page (Step 11)

- "The product page shows everything a consumer needs to make an informed decision: the description, the schema, who published it, and the quality contract."
- "The data contract is a formal agreement between the producer and the consumer — it defines the expected schema, quality rules, and SLA. Consumers know what they are getting before they subscribe."

### When showing the Subscription flow (Step 12)

- "The consumer submits a use case — this gives the data team visibility into how the data is being used across the organization."
- "The producer approves or rejects the request. This is the control point — data doesn't flow without an explicit approval."

### When showing data consumption (Step 13)

- "Once approved, the consumer can immediately download the data or access it programmatically — no waiting, no ticket queues."
- "The same data product is delivered in different formats depending on the user type: CSV for a business analyst, Arrow Flight for a data scientist's notebook."

---

## Key Business Value Points

| Value | One-liner |
|---|---|
| **Self-service access** | Consumers find and access data without raising a ticket |
| **Producer control** | Data teams see who uses what and can revoke access |
| **Trust through contracts** | Data quality is formally agreed upon, not assumed |
| **Reduced time-to-data** | From discovery to consumption in minutes |
| **Multiple delivery formats** | One product, many access patterns |
| **Reusability** | One curated dataset serves many teams |

---

## Common Audience Questions

**Q: How is this different from a data catalog?**
> A catalog helps you find and understand data. Data Product Hub goes further — it packages data assets into a versioned, governed product with a defined contract, delivery method, and access control. Think of it as moving from a library to a store.

**Q: Can the data contract be enforced automatically?**
> Yes. Data contracts follow the Open Data Contract Standard (ODCS) and can be enforced through the Data Contract Enforcement API. Quality checks run on a schedule defined in the contract.

**Q: What data sources are supported?**
> DPH supports SQL tables, SQL queries (parameterized), CSV files, and — when integrated with watsonx.data — direct Presto/Iceberg table access. ML models and BI dashboards are also supported as asset types.

**Q: Can this scale to an enterprise data mesh?**
> Yes. Each domain team acts as an independent data producer. DPH provides the federated marketplace layer where all domain products are discoverable centrally, while ownership stays with the domain teams.

---

## Upgrade Path (next steps after the demo)

If the audience wants to go deeper, position the upgrade options:

| Next Step | Adds |
|---|---|
| **Option 2: watsonx.data + DPH** | Lakehouse data sources, deliver-as-table method, parameterized queries |
| **Option 3: Cloud Pak for Data / Data Fabric** | IBM Knowledge Catalog, Manta lineage, data quality scoring, full governance |

---

[← Phase 4](phase-4-consumer-workflow.md) | [Back to README →](../README.md)
