# Phase 5 — Demo Talking Points

[← Phase 4](phase-4-consumer-workflow.md) | [Back to README →](../README.md)

---

Use this phase as a reference while delivering the demo to a customer or stakeholder audience.

---

## Story Arc

### The Problem (set context before the demo)

> _"Today, data consumers — analysts, data scientists, and business users — waste days or weeks trying to find data. When they do find it, they don't know if it's trustworthy, up to date, or approved for their use case. They raise tickets, send emails, and wait. Meanwhile, data engineers are buried in ad-hoc data requests instead of building pipelines."_

### The Solution (transition into the demo)

> _"IBM Data Product Hub, powered by watsonx.data, turns data into a product — something that is curated, documented, governed, and delivered through a self-service marketplace. The data stays live in the lakehouse. There are no stale copies. Let me show you how that works from both sides."_

---

## Talking Points by Demo Step

### When showing the Marketplace (Step 12)

- "This is the data marketplace — a single place where consumers can find all approved, curated data products across the organization, all sourced from the enterprise lakehouse."
- "Notice the search and filters. Consumers can filter by domain, tags, or asset type. No need to know which team owns the data or where it lives in the lakehouse."

### When showing the Data Product Detail page (Step 13)

- "The product page shows everything a consumer needs to make an informed decision: the description, the schema, who published it, and the quality contract."
- "Notice the schema is live — it is pulled directly from the Presto engine on watsonx.data. This is not a manually maintained documentation page."
- "The data contract is a formal agreement between the producer and the consumer — it defines the expected schema, quality rules, and SLA. Consumers know what they are getting before they subscribe."

### When showing the Subscription flow (Step 14)

- "The consumer submits a use case — this gives the data team visibility into how the data is being used across the organization."
- "The producer approves or rejects the request. This is the control point — data access doesn't flow without an explicit approval, even though the consumer experience feels self-service."

### When showing Data Extract (Step 15, Option A)

- "Once approved, the consumer can immediately download the data. No waiting, no ticket queues — from discovery to CSV in under two minutes."

### When showing Access in watsonx.data (Step 15, Option B)

- "This is the powerful option for technical consumers. Instead of downloading a copy, the consumer gets governed access to query the live lakehouse data directly — through a secure, producer-controlled channel."
- "No data movement. No duplication. The lakehouse stays as the single source of truth, and the producer can revoke access at any time."

### When showing Deliver as a Table (Step 15, Option C)

- "For consumers who need the data in their own lakehouse namespace — perhaps for a BI pipeline or a downstream transformation — DPH can materialise the data product as a new Iceberg table. One click. Fully governed."

---

## Key Business Value Points

| Value | One-liner |
|---|---|
| **Self-service access** | Consumers find and access data without raising a ticket |
| **Live lakehouse data** | Data is sourced directly from watsonx.data — no stale copies |
| **Producer control** | Data teams see who uses what and can revoke access |
| **Trust through contracts** | Data quality is formally agreed upon, not assumed |
| **Reduced time-to-data** | From discovery to consumption in minutes |
| **Multiple delivery formats** | CSV for analysts, live access for engineers, table delivery for pipelines |
| **No data duplication** | Access in watsonx.data shares a governed view — not a copy |

---

## Common Audience Questions

**Q: How is this different from a data catalog?**
> A catalog helps you find and understand data. Data Product Hub goes further — it packages data assets into a versioned, governed product with a defined contract, delivery method, and access control. Think of it as moving from a library to a store.

**Q: Does the data move when a consumer subscribes?**
> Not with the "Access in watsonx.data" delivery method. The consumer gets a governed pointer to the live lakehouse resource. With "Data Extract," a snapshot is created on demand. With "Deliver as a Table," the data is materialized once into the consumer's namespace.

**Q: Can the data contract be enforced automatically?**
> Yes. Data contracts follow the Open Data Contract Standard (ODCS) and can be enforced through the Data Contract Enforcement API backed by the watsonx.data intelligence data quality engine.

**Q: What data sources are supported?**
> With watsonx.data, DPH supports Presto-queryable sources: Iceberg tables, Hive tables, and any data source connected via a Presto connector (Db2, PostgreSQL, MySQL, S3/Parquet, and more). SQL queries (parameterized) are also supported.

**Q: Can this scale to an enterprise data mesh?**
> Yes. Each domain team acts as an independent data producer publishing to the shared marketplace. DPH provides the federated marketplace layer — products are discoverable centrally while ownership and governance stay with the domain teams. watsonx.data provides the shared lakehouse infrastructure underneath.

**Q: What is the difference between watsonx.data and watsonx.data intelligence in this bundle?**
> watsonx.data is the open lakehouse engine (Presto, Iceberg, object storage). watsonx.data intelligence adds the governance layer on top — IBM Knowledge Catalog for metadata, Manta for lineage, and data quality scoring. In this demo, intelligence powers the data contract enforcement and trust indicators you see in DPH.

---

## Upgrade Path (next steps after the demo)

| Next Step | Adds |
|---|---|
| **Enable IBM Knowledge Catalog** | Governed asset catalogue, business terms, data classifications — assets promoted from IKC directly into DPH |
| **Enable Manta Data Lineage** | End-to-end lineage from source system through lakehouse to data product |
| **Enable data quality scoring** | Automated quality scores surfaced on the marketplace listing |
| **Add more data domains** | Expand to Finance, HR, Operations — show a true multi-domain data mesh |

---

[← Phase 4](phase-4-consumer-workflow.md) | [Back to README →](../README.md)
