# Snowflake Terminology — Quick Distinctions

## Warehouses
- Scale Up = bigger warehouse.
- Scale Out = more clusters.
- Standard policy = prioritize reducing queueing.
- Economy policy = prioritize credit savings.

## Caches
- Query Result Cache = reusable result; no warehouse required.
- Metadata Cache = metadata-derived information.
- Warehouse Cache = local data cache; lost on suspend/resize.

## Governance
- Masking = columns.
- Row Access Policy = rows.
- Tagging = classification/metadata.
- Lineage = origin/downstream flow.
- Trust Center = security posture/recommendations.
- DMF = data quality.

## Integrations
- Storage Integration = cloud storage access.
- API Integration = external API/service access.
- Git Integration = repository/version-control access.

## Collaboration
- Share = live read-only data access.
- Reader account = provider-managed consumer account.
- Clean Room = controlled multi-party analysis.
- Clone = logical copy.
- Iceberg = open table format.

## AI
- Cortex Search = search in text/documents.
- Cortex Analyst = natural-language questions over tables.
- LLM functions = generation, summarization, translation, sentiment, extraction, embeddings.
- Snowflake ML = ML lifecycle inside Snowflake.
