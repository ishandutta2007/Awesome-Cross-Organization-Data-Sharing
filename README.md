# Awesome-Cross-Organization-Data-Sharing

# Awesome-Cross-Organization-Data-Sharing
**Top Cross Organization Data Sharing (Opensource) 🌟 Star if you like it! 🌟**

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on Zero-Copy Sharing, Open Protocols, Data Clean Rooms & Self-Hosted Exchange Infrastructure*
**Last updated: November 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Cross-Organization Data Sharing**. These tools enable organizations to share live data with partners, suppliers, and customers without copying or moving it—from fully managed enterprise platforms with governance and monetization to open protocols and self-hosted exchanges that give organizations control over their data sharing infrastructure.

**Examples** include Snowflake Data Sharing, Databricks Delta Sharing (OpenSharing), AWS Data Exchange, Azure Data Share, Dawex, Harbr, ThinkData Works, LiveRamp Safe Haven, InfoSum, and Revelate (the category leaders in commercial space).

**Open-source emphasis**: This section is expanded with every relevant project for self-hosted data sharing, open protocols, and federated exchange infrastructure. **Critical note**: The open-source landscape is anchored by **OpenSharing** (formerly Delta Sharing)—a Linux Foundation project that defines a vendor-neutral protocol for zero-copy sharing of tables, volumes, models, and agent skills across any platform . This is the most significant open-source development in the category. No open-source project matches Snowflake's managed reader account simplicity or InfoSum's privacy-preserving matching, but for protocol-level interoperability, OpenSharing is production-proven.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Snowflake Data Sharing](https://www.snowflake.com/)**
  **Native zero-copy data sharing** within Snowflake. **Direct Share**: share with any Snowflake account in the same region—no data duplication, no ETL; recipient uses their own compute and role-based access controls . **Reader Accounts**: provider provisions a Snowflake account for recipients without a subscription; limited by a consumption quota (e.g., 20 credits); compute costs bill to the provider . **Pricing**: Included with Snowflake; provider pays for reader account compute; Snowflake Marketplace listings can be paid with usage-based or subscription pricing . **Free tier**: Trial credits available. **Best for**: Snowflake customers wanting governed, zero-copy sharing within the Snowflake ecosystem—**trade-off**: direct shares are region-bound; reader accounts put compute costs on the provider.

- **[Databricks Delta Sharing / OpenSharing](https://www.databricks.com/product/delta-sharing)**
  **Open protocol for cross-platform data and AI asset sharing**, now evolved to **OpenSharing** under Linux Foundation governance . **Features**: Zero-copy sharing of tables (Delta Lake, Iceberg, Parquet), volumes, models, notebooks, and agent skills; **credential vending**—recipients access assets directly from the provider's storage via short-lived, scoped credentials; works across clouds (S3, ADLS, GCS, R2) and platforms; **Unity Catalog integration** for centralized governance; **Databricks Marketplace** for discovering data products; **Clean Rooms** for privacy-preserving collaboration . **Pricing**: Consumption-based (DBUs) for Databricks platform; OpenSharing protocol itself is Apache 2.0 and free. **Free tier**: Community Edition limited. **Best for**: Databricks customers and multi-platform organizations wanting vendor-neutral sharing of data and AI assets—**trade-off**: full managed experience requires Databricks; protocol adoption requires compatible clients.

- **[AWS Data Exchange](https://aws.amazon.com/data-exchange/)**
  **Marketplace for third-party data products** with AWS billing integration. **Pricing models**: Fixed-fee subscription (dominant, most negotiable—20–40% off list via private offers), per-record/per-API-call, trial+subscription, and private offers . **EDP eligibility**: Annual fixed-fee subscriptions usually EDP-eligible; per-record often not . **Egress costs** can equal or exceed subscription fees for multi-TB products . **Free tier**: Trial products available; no permanent free tier. **Best for**: enterprises subscribing to multiple data providers wanting consolidated AWS billing and entitlement management—**trade-off**: egress economics frequently overlooked; EDP eligibility varies by product.

- **[Azure Data Share](https://azure.microsoft.com/en-us/products/data-share)**
  **Snapshot-based data sharing** within Azure. **Pricing**: Provider is billed for **Dataset Snapshot** (per dataset moved) and **Snapshot Execution** (vCores × duration, prorated by minute) . **Free tier**: Not specified. **Best for**: Azure-centric organizations wanting simple snapshot-based sharing to partners—**trade-off**: snapshot-based, not live/zero-copy; provider bears all costs.

- **[Dawex](https://www.dawex.com/)**
  **Data exchange platform** for monetizing and sharing data products. **Pricing models**: File-based (one-off or subscription), API Pull (per volume, per duration, per quota, or per unit), API Push (per access duration) . **Free tier**: Not specified. **Best for**: organizations wanting to monetize data products with flexible pricing models—**trade-off**: platform fees; enterprise-focused.

- **[Harbr](https://www.harbrdata.com/)**
  **Enterprise data exchange platform** for building custom-branded data marketplaces. **Features**: Connect any data source; convert to data products; granular access controls; secure collaboration workspaces; publish to custom-branded store . **Deployment**: Pairs your AWS/Azure/GCP VPC with Harbr's—you retain data, Harbr brings software . **Pricing**: Quote-only. **Free tier**: None. **Best for**: enterprises wanting a private, branded data exchange without building from scratch—**trade-off**: enterprise pricing; VPC integration required.

- **[ThinkData Works (Namara)](https://www.thinkdataworks.com/)**
  **Public data aggregation and standardization** platform. Namara standardizes, reformats, and enriches public data from 1,000+ sources and 100,000+ datasets . **Pricing**: Quote-only. **Free tier**: Not specified. **Best for**: organizations wanting curated public/alternative data—**note**: this is public data aggregation, not cross-organization private sharing.

- **[LiveRamp Safe Haven](https://liveramp.com/)**
  **Privacy-preserving data clean room** for collaboration. **APIs**: Job Management API for scheduling PySpark/BigQuery jobs; Cleanroom API, Datasets API, Exports API, and Flow Runs API . **Pricing**: Quote-only. **Free tier**: None. **Best for**: advertisers and publishers wanting privacy-safe data collaboration—**trade-off**: clean room, not a general data exchange.

- **[InfoSum](https://www.infosum.com/)**
  **Decentralized data collaboration** platform with **Beacons** deployed inside your Snowflake account. **Features**: Connect datasets across companies and clouds without moving raw data; vector-based matching; privacy-safe outputs; source data stays in your Snowflake account . **Pricing**: Free app + Snowflake infrastructure cost; requires InfoSum Platform account and Beacon license . **Free tier**: App is free; platform license required. **Best for**: enterprises wanting privacy-preserving matching without data movement—**trade-off**: requires InfoSum platform account; Snowflake-specific Beacon deployment.

- **[Revelate](https://www.revelate.com/)**
  **Self-serve data marketplace** for governed data product delivery within organizations. **Features**: Integrates with existing data platforms; package data, apply access controls, deliver to internal and external users; automates distribution workflows . **Pricing**: Quote-only; Gartner Peer Insights lists product details but no public pricing . **Free tier**: Not specified. **Best for**: organizations wanting an internal data marketplace with self-service access—**trade-off**: quote-only; smaller vendor.

## Open-Source GitHub Projects

- **[OpenSharing (formerly Delta Sharing)](https://github.com/OpenSharing-IO/OpenSharing)**
  **The open sharing protocol for the agentic era** (Apache 2.0, Linux Foundation AI & Data Project) — **the most significant open-source project for cross-organization data sharing**, evolved from Delta Sharing . **Features**: **Vendor-neutral protocol**—any compliant client on any platform can consume any asset type without format-specific code. **Asset hierarchy**: Share → Schema → Asset. **Asset types**: **Table** (Delta Lake, Iceberg, Parquet), **Volume** (any file format—documents, media, embeddings), **AgentSkill** (reusable AI agent capabilities), **Model** (ML artifacts with provenance), plus community proposals for Agent and Page . **Zero-copy credential vending**—sharing server issues pre-signed URLs or temporary cloud credentials (AWS STS, Azure SAS, GCP OAuth, Cloudflare R2); recipients read directly from provider storage . **Works where data lives**—S3, ADLS, GCS, R2, on-premises . **Tech stack**: Protocol specification (Apache 2.0); reference implementations available. **Deploy**: Self-hosted sharing servers; compatible clients on any platform. **Trade-off**: **Protocol, not a product**—no managed UI, no billing integration, no reader account provisioning; you build or integrate the sharing server and client. **Best for**: organizations building cross-platform data sharing infrastructure wanting vendor neutrality and AI-asset coverage—especially those sharing tables, models, or agent skills across clouds and platforms.

### Additional Strong Open-Source Options

- **Delta Sharing (legacy)** — The original open protocol from Databricks/Linux Foundation (Apache 2.0). **Note**: Superseded by OpenSharing; legacy implementations remain functional but new development targets OpenSharing . **Best for**: existing Delta Sharing deployments evaluating migration to OpenSharing.
- **No mature open-source data exchange platform exists.** The category is dominated by proprietary vendors (Dawex, Harbr, Revelate) with no open-source equivalents for the marketplace/exchange layer. OpenSharing provides the protocol, not the exchange UI, billing, or governance workflows.

**Frameworks for building custom systems**: **OpenSharing** is the only open-source building block for cross-organization data sharing. For a complete stack, pair it with a custom sharing server implementation, a governance layer (e.g., OPA for access policies), and a marketplace UI built on the OpenSharing APIs. **No open-source project provides a turnkey data exchange platform comparable to Dawex or Harbr.**

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Cross-organization data sharing platforms handling partner data must comply with data protection regulations (GDPR, CCPA, etc.), data sharing agreements, and industry-specific regulations.
- **The "zero-copy sharing" vs. "snapshot sharing" vs. "clean room" vs. "marketplace" vs. "protocol" distinction is critical.** **Snowflake Data Sharing** and **Databricks Delta Sharing** provide **zero-copy live sharing**—data stays in place, recipients access directly . **Azure Data Share** is **snapshot-based**—data is copied at intervals, provider bears costs . **LiveRamp Safe Haven** and **InfoSum** are **clean rooms**—privacy-preserving matching, not general data exchange . **AWS Data Exchange**, **Dawex**, **Harbr**, and **Revelate** are **marketplaces/exchanges**—they add discovery, billing, and governance on top of sharing . **OpenSharing** is a **protocol**—it defines how sharing works but is not a product . **Choose based on whether you need live zero-copy access, snapshot copies, privacy-safe matching, a marketplace, or a protocol to build on.**
- **OpenSharing (formerly Delta Sharing) is the most important open-source development in this category.** It is a Linux Foundation project, Apache 2.0 licensed, and uniquely covers AI assets (models, agent skills) alongside tables and volumes . **The trade-off**: it is a protocol, not a product—no managed service, no UI, no billing. **For organizations building cross-platform sharing infrastructure, it is the foundation.**
- **Snowflake Reader Accounts shift compute costs to the provider.** If you share data with a partner via reader account, their queries bill to your Snowflake account . **Direct Share is preferable when the recipient has a Snowflake account**—they use their own compute .
- **AWS Data Exchange egress costs are the hidden trap.** For multi-TB data products, cross-region replication and access charges can equal or exceed subscription fees . **Architect for same-region delivery and use VPC endpoints for S3.**
- **Azure Data Share is snapshot-based, not live.** The provider pays for every dataset snapshot and execution . **For continuous sharing, Snowflake, Databricks, or OpenSharing are better choices.**
- **InfoSum Beacons run inside your Snowflake account**—source data never leaves . **This is a genuinely decentralized architecture**, but it requires both an InfoSum platform account and a Snowflake Beacon license.
- **Pricing opacity varies.** Snowflake, Databricks, and AWS publish consumption-based pricing. Azure publishes per-snapshot/execution pricing . Dawex publishes pricing models but not rates . Harbr, ThinkData Works, LiveRamp, InfoSum (platform), and Revelate require sales contact. **Validate with direct vendor conversations against your sharing volume and partner count.**
- Self-hosted open-source solutions require proper infrastructure (sharing servers, cloud storage access, credential management), security hardening, and ongoing maintenance. **Cross-organization sharing exposes data to external parties**—ensure your deployment includes scoped credentials, audit logging, and data sharing agreements before sharing production data.

---

**Made for data platform teams, partnership leads, and organizations building transparent cross-organization data sharing solutions.**
Let's make Cross-Organization Data Sharing more open, data-driven, and zero-copy-friendly.
