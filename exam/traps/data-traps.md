# Data Exam Traps

1. `FORCE = TRUE` forces reload behavior; `PURGE = TRUE` removes successfully loaded files.
2. `VALIDATION_MODE` validates without inserting.
3. Snowpipe = continuous file ingestion; Snowpipe Streaming = low-latency rows.
4. Storage Integration = cloud storage; API Integration = external APIs; Git Integration = repository.
5. Iceberg = open table format and cloud-storage interoperability.
6. External Table = query files in place.
7. Time Travel = user-accessible historical recovery/querying.
8. Fail-safe = additional recovery period handled by Snowflake support.
9. A cloned stream starts at the clone point and does not inherit pending original changes.
