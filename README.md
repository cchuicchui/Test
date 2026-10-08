# IBM Data Product Hub — Demo Guide

> A step-by-step guide to building an IBM Data Product Hub demo using the **watsonx.data intelligence Bundle (DPH Initialization)** environment on IBM TechZone.

## Overview

This guide walks you through setting up and running an **IBM Data Product Hub (DPH) demo** backed by a live **watsonx.data** lakehouse. The demo showcases the full producer/consumer data sharing experience — from publishing a data product sourced from Iceberg tables to consuming it via multiple delivery methods.

### What You Will Demo

| Persona | Experience |
|---|---|
| **Data Producer** | Connect to watsonx.data, create and publish a governed data product to the marketplace |
| **Data Consumer** | Discover, subscribe to, and consume a data product via CSV extract or live lakehouse access |

---

## Prerequisites

- IBM ID (for TechZone access)
- A browser that supports multiple profiles (e.g., Chrome) — to simulate two personas
- No local installation required — the demo runs entirely in the browser

---

## TechZone Environment

This guide is designed for the **"watsonx.data intelligence Bundle (DPH Initialization)"** collection on IBM TechZone.

| Service | Included | Role in Demo |
|---|---|---|
| **Data Product Hub** | ✅ | The marketplace — publish and consume data products |
| **watsonx.data** | ✅ | The lakehouse — Presto engine, Iceberg tables, object storage |
| **watsonx.data intelligence** | ✅ | Governance layer — data quality, lineage, IBM Knowledge Catalog |

> DPH is pre-initialized and pre-connected to watsonx.data in this bundle. No manual wiring is required.

---

## Demo Phases

| Phase | Description | Guide |
|---|---|---|
| 1 | Reserve TechZone Environment | [Phase 1 →](docs/phase-1-techzone-setup.md) |
| 2 | Initial Setup (Admin) | [Phase 2 →](docs/phase-2-admin-setup.md) |
| 3 | Producer Workflow | [Phase 3 →](docs/phase-3-producer-workflow.md) |
| 4 | Consumer Workflow | [Phase 4 →](docs/phase-4-consumer-workflow.md) |
| 5 | Demo Talking Points | [Phase 5 →](docs/phase-5-talking-points.md) |

---

## Quick Start

```bash
# No code installation required.
# This demo runs entirely in the browser using IBM TechZone SaaS services.
# Follow the phases in order, starting with Phase 1.
```

1. [Reserve your TechZone environment](docs/phase-1-techzone-setup.md)
2. [Set up services and user personas](docs/phase-2-admin-setup.md)
3. [Run the Producer workflow](docs/phase-3-producer-workflow.md)
4. [Run the Consumer workflow](docs/phase-4-consumer-workflow.md)
5. [Deliver the demo with talking points](docs/phase-5-talking-points.md)

---

## Architecture

```
┌────────────────────────────────────────────────────────────┐
│                IBM Data Product Hub (SaaS)                 │
│                                                            │
│  ┌──────────────────────┐    ┌───────────────────────┐     │
│  │      Producer        │    │  Consumer Marketplace │     │
│  │                      │    │                       │     │
│  │  - Upload data       │    │  - Browse & search    │     │
│  │  - Add assets        │───▶│  - View data contract │     │
│  │  - Set data contract │    │  - Subscribe          │     │
│  │  - Publish           │    │  - Download / access  │     │
│  └──────────────────────┘    └───────────────────────┘     │
└────────────────────────────────────────────────────────────┘
              │ Presto connection              │
              ▼                               ▼
┌────────────────────────────────────────────────────────────┐
│                    IBM watsonx.data                        │
│                                                            │
│   Iceberg Tables  │  Presto Engine  │  Object Storage      │
│                                                            │
│  (governed by watsonx.data intelligence:                   │
│   Knowledge Catalog · Data Quality · Lineage)              │
└────────────────────────────────────────────────────────────┘
```

---

## Reference

| Resource | Link |
|---|---|
| IBM TechZone | https://techzone.ibm.com |
| DPH Documentation | https://www.ibm.com/docs/en/cloud-paks/cp-data |
| watsonx.data Documentation | https://www.ibm.com/docs/en/watsonxdata |
| DPH + watsonx.data Integration | https://www.ibm.com/docs/en/watsonxdata?topic=integrations-integrating-data-product-hub |
| Open Data Contract Standard (ODCS) | https://bitol-io.github.io/open-data-contract-standard/latest/ |

---

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

[Apache 2.0](LICENSE)
