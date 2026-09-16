# Architecture Exam Traps

1. One complex query or memory pressure → think **Scale Up**.
2. Many simultaneous users or queueing → think **Scale Out / Multi-cluster**.
3. Result cache does not require a running warehouse.
4. Warehouse cache requires the warehouse and is lost after suspend/resize.
5. Snowpark-optimized is for memory-intensive Snowpark/ML workloads.
6. More-specific parameter levels override broader levels.
7. Do not confuse materialized views with secure views.
