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

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## Sector Overview & Market Dynamics

The global Data Sharing-as-a-Service (DSaaS) market is valued at approximately **$3.97B to $4.2B** (with the privacy-focused data clean room subsegment representing ~$1.4B–$1.9B), expanding at an 18–21% CAGR. The sector is **moderately fragmented yet increasingly bifurcated**: core compute/storage-level zero-copy sharing exhibits winner-take-all dynamics concentrated among hyperscale cloud data platforms (Microsoft, AWS, Snowflake, Databricks), while privacy-enhancing clean rooms, independent commercial exchanges, and cross-party federation remain fragmented among specialized vendors (Dawex, Harbr, InfoSum, LiveRamp).

## SaaS/Hosted Platforms

| Platform | Company Size (Revenue / Valuation) | Starting Pricing Tier | Free Tier Limits / Free Trial | Key Capabilities & Trade-offs |
| :--- | :--- | :--- | :--- | :--- |
| **[Azure Data Share](https://azure.microsoft.com/en-us/products/data-share)** | **$3.1T+** Market Cap (Microsoft) | **$0.05 / dataset-snapshot** + **$0.50 / vCore-hour** execution (prorated by minute) | **30-Day Free Trial** with **$200 Azure credits**; includes access to 55+ always-free Azure services (standard Azure storage/compute charges apply after credits) | Snapshot-based sharing across Azure tenants. Provider pays all snapshot and compute costs; data is copied rather than queried via zero-copy. |
| **[AWS Data Exchange](https://aws.amazon.com/data-exchange/)** | **$2.1T+** Market Cap (Amazon) | **3% fulfillment fee** on data transactions + **$0.04167/hour** per active data grant + S3 storage ($0.023/GB/mo) | **AWS Free Tier (12 months free / always-free limits)** plus provider-specific **free trial data products** (e.g., 7–30 day trial access to selected public/commercial datasets) | Cloud-native data marketplace integrated with AWS billing and EDP drawdowns. Egress fees can escalate on multi-TB products; private offers negotiable. |
| **[Snowflake Data Sharing](https://www.snowflake.com/)** | **~$50B** Market Cap | **$2.00 / credit** (Standard Edition) to **$3.00 / credit** (Enterprise Edition) compute consumption | **30-Day Free Trial** with **$400 in free usage credits** (no permanent free tier; Reader Accounts allow recipients to query without paid subscriptions, billed to provider) | Native zero-copy data sharing without ETL or data movement. Reader accounts enable sharing with non-Snowflake customers but push compute expenses to provider. |
| **[Databricks Delta Sharing / OpenSharing](https://www.databricks.com/product/delta-sharing)** | **$43B** Valuation / **$2.6B+ ARR** | **$0.07 / DBU** (Standard Plan) to **$0.55 / DBU** (Enterprise Jobs/Compute) | **14-Day Free Trial** on full cloud platform; **Databricks Community Edition** is free forever with 1 micro-cluster (15GB single node, Delta Sharing hosting excluded) | Open zero-copy sharing of tables, volumes, models, and agent skills via credential vending. Built on open OpenSharing protocol, managed via Unity Catalog. |
| **[LiveRamp Safe Haven](https://liveramp.com/)** | **~$2.0B** Market Cap (NYSE: RAMP) / **~$750M ARR** | **$20,000 / year** (Standard Tier for <5M customer records and 1–3 destinations) | **No Free Tier or Self-Serve Trial**; evaluation requires a guided custom Proof of Concept (PoC) or guided interactive sandbox demo | Privacy-preserving enterprise data clean room and identity resolution engine for multi-party marketing and analytics. |
| **[InfoSum](https://www.infosum.com/)** | **~$150M** Acquisition Value (WPP) / **~$10M–$15M ARR** | **~$3,000 / month** base platform contract (or private offer via AWS/GCP/Snowflake marketplaces) | **No Free Tier or Self-Serve Trial**; requires custom enterprise contract or proof-of-concept; Snowflake Native App Beacons free to deploy but require platform license | Decentralized data collaboration with Bunkers and Snowflake Beacons. Raw data never moves; privacy-safe vector matching across clouds. |
| **[Harbr](https://www.harbrdata.com/)** | **~$169M** Valuation / **~$50M** Total Raised | **~$2,500 / month** ($30,000/yr starting enterprise pilot deployment) | **No Free Tier or Self-Serve Trial**; evaluation is restricted to custom private enterprise sandbox walkthroughs and sales demos | White-label data commerce and marketplace platform connecting existing VPCs; enables custom branded enterprise data exchanges. |
| **[Revelate](https://www.revelate.com/)** | **~$100M–$150M** Est. Valuation / **~$10M–$20M ARR** | **~$2,000 / month** ($25,000/yr starting enterprise data distribution license) | **No Free Tier or Self-Serve Trial**; prospective buyers must request a custom platform demonstration and guided evaluation trial | Turnkey data marketplace and fulfillment engine (formerly TickSmith); automates external packaging and commercialization workflows. |
| **[Dawex](https://www.dawex.com/)** | **~$50M–$80M** Est. Valuation / **~$9.6M ARR** | **~$1,500 / month** (€18,000/yr baseline private data exchange SaaS license) | **No Free Tier or Self-Serve Trial**; access is restricted to structured corporate demos and pilot evaluations | Enterprise data exchange software powering corporate and regional trusted data spaces complying with European Data Governance Act frameworks. |
| **[ThinkData Works (Namara)](https://www.thinkdataworks.com/)** | **~$15M–$25M** Est. Valuation / **~$2.2M ARR** | **~$1,000 / month** ($12,000/yr starter data catalog & marketplace tier) | **No Free Tier or Self-Serve Trial**; offers personalized product walkthroughs and 14-day assisted enterprise trials upon qualification | Focuses on public/alternative data aggregation, cataloging, and automated enrichment across 100K+ external public sources. |

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
