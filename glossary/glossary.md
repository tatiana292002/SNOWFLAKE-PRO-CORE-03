# SnowPro Core Glossary

**Cloud Services** — Snowflake layer for authentication, access control, metadata, optimization, and security.

**Virtual Warehouse** — Compute engine for queries and loading work.

**Micro-partition** — Snowflake storage unit, approximately 50–500 MB in the guide, with metadata used for pruning.

**Pruning** — Skipping micro-partitions that cannot satisfy a filter.

**Scale Up** — Increase warehouse size.

**Scale Out** — Add warehouse clusters.

**Query Result Cache** — Reusable query-result cache in Cloud Services.

**Warehouse Cache** — Local/SSD cache associated with a running warehouse.

**RBAC** — Role-Based Access Control.

**DAC** — Discretionary Access Control.

**Masking Policy** — Controls presentation of sensitive column values.

**Row Access Policy** — Controls which rows are visible.

**Tag** — Governance/classification metadata attached to objects or columns.

**Data Lineage** — Information about data origin and downstream flow.

**DMF** — Data Metric Function used for automated data-quality measurements.

**Stage** — File location/reference used for loading and unloading.

**COPY INTO** — Command for loading data into tables or unloading data to stages.

**Snowpipe** — Continuous file ingestion.

**Snowpipe Streaming** — Low-latency row ingestion.

**Dynamic Table** — Declarative transformation maintained toward a freshness target.

**Stream** — Change-tracking object.

**Task** — Scheduled/triggered execution of SQL or procedural work.

**Secure Data Share** — Live, read-only sharing without copying provider data.

**Reader Account** — Provider-managed Snowflake account for a consumer without Snowflake.

**Data Clean Room** — Controlled multi-party analysis without exposing raw participant data.

**Zero-Copy Clone** — Logical copy using metadata/copy-on-write.

**Iceberg Table** — Open table format with data in cloud storage and interoperability with other engines.

**Cortex Search** — Semantic/hybrid search over text/documents.

**Cortex Analyst** — Natural-language questions over tables that result in SQL execution.
