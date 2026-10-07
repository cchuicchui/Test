# IBM Data Product Hub — Standalone Demo Guide

> A step-by-step guide to building an IBM Data Product Hub demo using IBM TechZone resources.

## Overview

This guide walks you through setting up and running an **IBM Data Product Hub (DPH) Standalone demo** — the fastest path to demonstrating the producer/consumer data sharing experience without requiring the full Data Fabric stack.

### What You Will Demo

| Persona | Experience |
|---|---|
| **Data Producer** | Create, document, and publish a data product to the marketplace |
| **Data Consumer** | Discover, subscribe to, and consume a data product |

---

## Prerequisites

- IBM ID (for TechZone and IBM Cloud access)
- A browser that supports multiple profiles (e.g., Chrome) — to simulate two personas
- Sample dataset (CSV) — see [sample data suggestions](docs/sample-data.md)

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
# This demo runs entirely in the IBM Data Product Hub SaaS UI.
# Follow the phases in order, starting with Phase 1.
```

1. [Reserve your TechZone environment](docs/phase-1-techzone-setup.md)
2. [Set up users and personas](docs/phase-2-admin-setup.md)
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
```

---

## Reference

| Resource | Link |
|---|---|
| IBM TechZone | https://techzone.ibm.com |
| DPH Documentation | https://www.ibm.com/docs/en/cloud-paks/cp-data |
| DPH Video Library | Available in CPD docs → Video library → Use Data Product Hub |
| Open Data Contract Standard (ODCS) | https://bitol-io.github.io/open-data-contract-standard/latest/ |

---

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

[Apache 2.0](LICENSE)
