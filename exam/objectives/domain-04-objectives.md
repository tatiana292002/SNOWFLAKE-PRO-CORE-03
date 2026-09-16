# Domain 4 Objectives — Performance, Querying, and Transformation

**Weight: 21%**

1. Diagnose queries with Query Profile.
2. Recognize spilling and queueing symptoms.
3. Diagnose inefficient pruning.
4. Diagnose exploding joins.
5. Distinguish warehouse resizing, multi-cluster, SOS, clustering, materialized views, and QAS.
6. Understand workload management.
7. Use ACCOUNT_USAGE and query attribution for monitoring.
8. Understand caching as a performance lever.
9. Understand Streams and Tasks.
10. Understand Dynamic Tables and TARGET_LAG.
11. Understand SCD Types 1, 2, and 3.
12. Understand UDFs, UDTFs, and stored procedures as described by the guide.
13. Transform structured, semi-structured, and unstructured data.
14. Recognize aggregation and window-function usage.

### Scenario rules
- Concurrency/queue → multi-cluster
- Individual memory pressure → larger warehouse
- Point lookup → SOS
- Repeated filtering pattern → clustering
- Repeated expensive aggregation → materialized view
- Large unpredictable scan spike → QAS
- Exploding join → fix SQL logic
