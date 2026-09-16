# Performance Exam Traps

1. Exploding JOIN → inspect/fix join logic and cardinality.
2. Point/selective lookup on a huge table → Search Optimization.
3. Repeated filtering/ordering pattern → clustering may improve pruning.
4. Repeated expensive aggregation with relatively stable data → materialized view.
5. Unpredictable large scan spike → QAS.
6. Concurrency/queueing → multi-cluster, not a larger warehouse by default.
7. Separate ETL, BI, and ad-hoc workloads when contention is the issue.
8. Query Profile symptoms should drive the feature choice.
