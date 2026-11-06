## Hi 👋 I'm Anna

I'm a **Data Engineer** (with a Data Analyst background) who builds reliable, well-documented data platforms. I care about **idempotent pipelines**, **data quality**, and **clear definitions**, so that everyone trusts the same numbers.

Today I work on a Databricks lakehouse that powers real-time and batch analytics: event pipelines on **Kafka**, **Spark** and **Delta Lake**, orchestrated with **Dagster**, and served through **Druid** and **Rill**.

---

### 🛠 What I work with

| Area | Tools |
|---|---|
| **Lakehouse & processing** | Databricks (Unity Catalog, Workflows, serverless SQL), Apache Spark, Delta Lake, S3 |
| **Streaming & ingestion** | Kafka, Spark Structured Streaming, third-party feeds and APIs (MMPs, SSPs, market-intelligence data) |
| **Orchestration** | Dagster (assets, sensors, partitions), Airflow, GitHub Actions |
| **Serving & BI** | Druid, Rill (metrics views), ClickHouse, Grafana, Tableau |
| **Languages & modeling** | Python, SQL, dbt, medallion architecture (bronze / silver / gold) |
| **Quality & observability** | Freshness and completeness checks, data-quality alerting, Compass / Slack alerts, runbooks |

---

### 🔧 What I've been building recently

- **Idempotent, event-driven pipelines.** Hourly and daily slice writes (Delta `replaceWhere`, dynamic partition overwrite, Druid full replace) and Dagster sensors and fixed lags, so any partition can be re-run safely and published values don't change.
- **Druid ingestion tuning.** Cut a heavy daily ingestion from **~7.8 h to ~3.3 h** by diagnosing peon out-of-memory failures, disabling unneeded lookup loading and tuning `maxRowsInMemory`, then rolling the fix out to the other batch specs.
- **Pipeline reliability and guardrails.** Added partition-materialization checks, retries with clear error reporting for flaky Druid SQL calls, and alert schedules aligned to real landing times to remove false alarms.
- **Third-party data into the lakehouse.** Turned a vendor's raw S3 drops (31 feeds) into maintained Delta mirrors with freshness and duplicate checks. Wrote a design for loading the remaining ~2 TB of feeds with cadence-aware, incremental upserts and batched backfills.
- **AI cost tracking.** Combined card spend, Codex and Claude usage into one cost model. Explained a ~$18K monthly gap between a dashboard and the vendor export (credit pricing, dropped records, chat usage), and moved the pipeline from a Databricks job into Dagster with parity checks.
- **Query performance in Rill and Druid.** Replaced calculated dimensions with stored columns and live JDBC lookups; one filter went from **41.7 s to ~0.5 s**. Cut roughly 720 lines of precomputed lookup code by switching to live lookups.
- **Data-quality and source reconciliation.** Built a maintained discrepancy-monitoring system across SDK, MMP and BI sources (dashboards as code, a gold table, a runbook) and validation steps for ML training datasets.

---

### 📚 Background

I got into data in 2020 and learned **dbt**, **Airflow** and **Tableau** on challenging projects that pushed me deep into **SQL** and **Python**.

My student project was a fun one: my team used NLP (sentiment analysis, topic classification, text generation) to build a model that writes in the style of a teenager's diary. [Sorry, it's in Russian](https://projects.pandan.eusp.org/feelings), but there are cool pictures.

Before data engineering full time, I worked at:

- an **NGO** improving policy-making with a scientific approach, analysing large volumes of governmental data;
- a **fintech startup** using the latest LLMs to enrich transaction data.

---

### 🌱 Currently

- 🔭 Going deeper on **Dagster** and **Databricks / Spark** at scale
- 🌊 Sharpening **Delta Lake**, **Druid** and **Kafka streaming** patterns
- 🤝 Open to collaborating on challenging data engineering projects

### 📫 Reach me

[![Email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:01anna.timoshenko@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anna-timoshenko/)
