# Awesome-Data-Integration-ETL-Connectors

# Awesome-Data-Integration-ETL-Connectors

**Top Data Integration ETL Connectors (Opensource) 🌟 Star if you like it! 🌟**



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Managed ELT, CDC Replication, Connector Breadth & Self-Hosted Pipeline Frameworks*

**Last updated: November 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Data Integration & ETL Connectors**. These tools enable organizations to move data from databases, SaaS applications, and APIs into warehouses and lakes—from fully managed ELT platforms with 700+ connectors and automated schema handling to open-source frameworks that give teams complete control over their pipelines and deployment model.



**Examples** include Fivetran, Airbyte, Matillion, Qlik Replicate, Hevo Data, Informatica Cloud Data Integration, Boomi, Confluent Cloud, and Snowflake Connectors (the category leaders in commercial and open-source space).



**Open-source emphasis**: This section is expanded with every relevant project for self-hosted data integration, CDC replication, and open pipeline infrastructure. **Critical note**: The open-source landscape is anchored by **Airbyte**—the leading open-source ELT platform with 700+ connectors and a self-hosted Core edition . **Debezium** remains the standard for log-based CDC, **Apache NiFi** handles complex dataflow, and **dbt** transforms data after loading. No open-source project matches Fivetran's fully managed reliability, but for teams willing to operate infrastructure, Airbyte Core is production-proven.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The global data integration and ETL market is estimated at **$13.1B–$19.1B in 2025** and projected to reach **$14.3B–$21.5B by 2026** (~10–13% CAGR), fueled by cloud migration and enterprise AI data preparation pipelines. The market is **moderately fragmented**: hyperscalers and legacy enterprise providers (Microsoft, AWS, Google Cloud, Informatica, IBM) dominate core enterprise data fabric layers, while nimble modern ELT platforms (Fivetran, Airbyte, Matillion) and open-source frameworks continuously capture specialized pipeline and CDC workloads without a single winner-take-all monopoly.

## SaaS/Hosted Platforms

| Platform | Company Scale (Revenue / Valuation) | Pricing (Specific Starting Tiers) | Free Tier / Free Trial Limits | Description & Key Trade-offs |
| :--- | :--- | :--- | :--- | :--- |
| **[Snowflake Connectors](https://www.snowflake.com/en/developers/downloads/drivers-and-libraries/)** | **~$90B–$115B Market Cap** (~$4.5B+ annual revenue) | Connectors free; Snowflake warehouse compute starts at **Standard tier ~$2.00/credit** (On-demand) | **30-day free trial with $400 in free credits** (trial ends when credits exhaust or 30 days elapse) | Native client libraries (Snowpark, Python, Kafka, Spark). Fast native data transfer into Snowflake, but you must build and orchestrate the pipeline logic yourself. |
| **[Confluent Cloud](https://www.confluent.io/)** | **~$11B Enterprise Value / Market Cap** | Pay-as-you-go connector tasks from **$0.05–$0.10/task-hour** (e.g. S3 source) plus **$0.025/GB** data transfer | **30-day free trial with $400 in usage credits** (ends when credits exhaust or 30 days elapse) | Fully managed Apache Kafka data streaming with 100+ connectors. Best for event streaming pipelines; costs compound across task hours, partitions, and bandwidth. |
| **[Informatica Cloud Data Integration](https://www.informatica.com/)** | **~$7.5B–$8.0B Market Cap** (~$1.6B+ annual revenue) | Integration Cloud pay-as-you-go starts at **¥240,000/month (~$1,600/month)** or **$0.36/IPU-hour** (Informatica Processing Unit) | **30-day free trial** (provisioned evaluation organization with scoped IPU allowance for testing mappings and connectors) | Mature enterprise iPaaS with governance and complex data transformations. Best for large enterprises; steep learning curve and premium pricing. |
| **[Fivetran](https://www.fivetran.com/)** | **$5.6B Valuation** | Free plan up to 500K MAR; Standard plan from **~$500 per million MAR**; **$12,000/year contract minimum**; **$5/month per standard connection** minimum | **Free plan forever up to 500,000 Monthly Active Rows (MAR)**; plus a **14-day unlimited free trial** on paid connectors | Fully managed ELT platform with 700+ connectors, merged with dbt Labs. Deletes and history-mode count toward paid MAR since Jan 2026, increasing high-churn costs. |
| **[Boomi Data Integration](https://boomi.com/)** | **~$4B Valuation** (acquired by Francisco Partners & TPG for $4B) | Pay-As-You-Go starts at **$99/month** (plus $0.05 per processed message); custom enterprise tiers from **$20,000+/year** | **30-day free trial** with full access to Boomi Enterprise Platform integration features (no upfront credit card required) | Low-code cloud-native iPaaS with distributed Atoms runtime. Well-suited for hybrid cloud and SaaS integration; advanced connectors require enterprise contracts. |
| **[Qlik Replicate](https://www.qlik.com/)** | **~$3B–$4B Est. Valuation** (~$750M+ annual revenue; Thoma Bravo owned) | Self-hosted/embedded starting at **$299/month flat rate** (per published entry listings; enterprise quote-based) | **30-day scoped PoC evaluation license** via sales request (license restricted to specified host machines and target endpoints; no public self-service tier) | High-throughput, real-time log-based CDC replication across heterogeneous databases. Best for legacy database sync; custom enterprise pricing required for high scale. |
| **[Airbyte Cloud](https://airbyte.com/)** | **$1.5B Valuation** (Series B) | Standard plan starts at **$20/month**; Plus plan at **$189/month**; Enterprise Flex capacity-based on Data Workers | **Self-hosted Core is 100% free forever**; Airbyte Cloud offers a **14-day free trial with $400 in usage credits** | Managed edition of the leading open-source ELT platform with 700+ connectors. Connector Builder allows fast custom APIs; capacity billing requires sync concurrency planning. |
| **[Matillion (Maia)](https://www.matillion.com/)** | **$1.5B Valuation** (Series E) | Credit-based consumption at **~$2.00 per credit** (Basic model starts at **$500/month** minimum commitment) | **14-day free trial with 500 free credits** (equivalent to ~$1,000 of platform compute) | Low-code pushdown pipeline and transformation platform for Snowflake, Databricks, Redshift, and BigQuery. Streaming CDC bills by clock hour (~1,440 credits/mo), not data volume. |
| **[Hevo Data](https://hevodata.com/)** | **~$100M–$250M Valuation** (~$46M annual revenue) | Free tier up to 1M events/month; Starter plan starts at **$239/month** (billed annually for 5M events/month) or **$299/month** (monthly billing) | **Free plan forever up to 1,000,000 events/month** (unlimited free sources, single destination, 12-hour sync frequency); **14-day free trial** with unlimited events | No-code ELT platform with 150+ pre-built connectors. Transparent, user-friendly entry point for small teams; event quotas deplete quickly on high-frequency streaming. |

## Open-Source GitHub Projects



- **[Airbyte (Core)](https://github.com/airbytehq/airbyte)**

  **Open-source data movement for ELT pipelines** (Elastic License 2.0 for core) — **the leading open-source ELT platform** with 700+ connectors and a self-hosted Core edition . **Features**: **Connector Builder** with AI assist (minutes, no code); **low-code CDK and Python CDK** for custom connectors; **PyAirbyte** for Python-native integration; **Terraform provider**; runs self-hosted, managed, hybrid, or on-prem on one codebase . **Tech stack**: Java (platform), Python (connectors). **Deploy**: Self-hosted (Docker) or Airbyte Cloud. **Trade-off**: **Operational overhead**—self-hosted Airbyte requires maintenance; connector quality varies. **Best for**: teams wanting the broadest open-source connector coverage without per-row SaaS costs—the pragmatic default for self-hosted ELT.



- **[Debezium](https://github.com/debezium/debezium)**

  **Open-source distributed platform for change data capture** (Apache 2.0) — **the de facto standard for log-based CDC**. **Features**: Captures row-level changes from MySQL, PostgreSQL, MongoDB, Oracle, SQL Server, Db2, and more; streams into Kafka topics; **Kafka Connect compatible** with horizontal scaling; snapshot + incremental switching with exactly-once semantics. **Tech stack**: Java. **Deploy**: Kafka Connect, Debezium Server, or embedded. **Trade-off**: **Requires Kafka for Kafka Connect deployment**—adds operational overhead. **Best for**: teams with existing Kafka infrastructure needing CDC with multi-consumer fanout.



- **[Apache NiFi](https://github.com/apache/nifi)**

  **Dataflow automation with browser-based UI** (Apache 2.0) — **the most mature open-source dataflow tool**. **Features**: Visual design and monitoring; **provenance tracking** with data lineage; guaranteed delivery with retry/backoff; horizontal scaling with clustering; extensible processors. **Tech stack**: Java. **Deploy**: Self-hosted. **Trade-off**: **Heavier than library-first tools**—requires Java runtime and operational management. **Best for**: organizations needing complex dataflow orchestration with visual design and provenance.



- **[dbt (data build tool)](https://github.com/dbt-labs/dbt-core)**

  **SQL-based transformation framework** (Apache 2.0) — **the standard for post-load transformation**. **Features**: Write transformations as SQL SELECT statements; dbt handles materialization (tables, views, incremental); **lineage and documentation** auto-generated; testing framework; **Fivetran acquired dbt Labs June 2026**—dbt remains open source but now bundled with Fivetran . **Tech stack**: Python, SQL. **Deploy**: Self-hosted (dbt Core) or dbt Cloud. **Trade-off**: **Transformation only**—no extraction or loading; pair with Airbyte or Fivetran for ELT. **Best for**: analytics engineers wanting version-controlled, tested SQL transformations—the complement to any ingestion tool.



### Additional Strong Open-Source Options



- **Apache SeaTunnel** — Distributed data integration (Apache 2.0). Batch and CDC synchronization at scale; multi-engine support (Zeta, Flink, Spark). **Note**: Steeper operational learning curve than Airbyte. **Best for**: high-volume batch and CDC synchronization with engine flexibility.

- **dlt (data load tool)** — Library-first data loading (Apache 2.0). `pip install dlt`; Python-native pipelines; 20+ destinations. **Note**: Library, not a platform—you own orchestration. **Best for**: Python developers wanting maintainable, testable pipelines in their codebase.

- **Kafka Connect JDBC Source** — Query-based CDC via polling. **Note**: **Does not capture deletes**; avoid unless binlog access is impossible. **Best for**: legacy systems without transaction log access.



**Frameworks for building custom systems**: Combine **Airbyte Core** for broad connector coverage with **Debezium** for log-based CDC into Kafka, **dbt** for transformation, and **Apache NiFi** for complex dataflow—creating a complete open-source ELT stack. **None of these match Fivetran's fully managed reliability**, but for teams prioritizing cost control and data ownership, the open-source options cover virtually every integration pattern.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Data integration platforms handling production data must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate encryption, access controls, and audit logging.

- **The "managed ELT" vs. "CDC replication" vs. "transformation" vs. "connector library" distinction is critical.** **Fivetran, Airbyte Cloud, Hevo, and Informatica** are **managed ELT**—they extract, load, and often transform . **Qlik Replicate** and **Debezium** are **CDC replication**—they capture changes from databases . **Matillion** is **transformation-focused**—it runs SQL in your warehouse . **Snowflake Connectors** are **connector libraries**—you build the pipeline logic . **dbt** is **transformation only**—pair with an ingestion tool. **Choose based on whether you need managed convenience, CDC depth, in-warehouse transformation, or custom integration code.**

- **Fivetran's MAR billing changes materially affect cost.** Since January 2026, deletes and history-mode changes count toward paid MAR; per-connection billing removed account-wide volume discounts. Third-party analyses report **40–70% cost increases** for multi-connector teams . **Model your row churn before committing.**

- **Matillion's CDC billing is a trap.** Streaming CDC bills by the clock—a premium stream runs **~720 hours/month (~1,440 credits)** whether one row or a billion changes . **Always-on CDC is expensive; warehouse compute is a second bill.**

- **Airbyte Core is the strongest open-source ELT foundation.** 700+ connectors, Connector Builder with AI assist, and self-hosted deployment on one codebase . **The trade-off**: operational overhead and variable connector quality.

- **Hevo's free tier is genuinely usable**—1M events/month, unlimited free sources, no credit card . **For small teams testing ELT, it is the pragmatic starting point.**

- **Confluent's connector pricing varies widely.** S3 source is $0.05–$0.10/task-hour; Couchbase is $0.30/task-hour; CDC connectors are contact-us . **Model your specific connector mix before committing.**

- **Pricing opacity varies.** Fivetran, Airbyte, Matillion, Hevo, Qlik, Informatica, Boomi, and Confluent all publish some pricing or calculators, but enterprise tiers require sales contact. **Validate with direct vendor conversations against your data volume and connector requirements.**

- Self-hosted open-source solutions require proper infrastructure (PostgreSQL for Airbyte, Kafka for Debezium, Java for NiFi), security hardening, and ongoing maintenance. **Data integration pipelines handle production data**—ensure your deployment meets your organization's security standards before connecting production systems.



---



**Made for data engineers, analytics teams, and organizations building transparent data integration solutions.**

Let's make Data Integration & ETL Connectors more open, data-driven, and pipeline-reliable.
