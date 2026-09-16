# Security Exam Traps

1. SELECT alone is not enough: check database/schema USAGE and warehouse USAGE.
2. RBAC = privileges through roles; DAC = ownership controls the object.
3. Managed access centralizes object privilege grants.
4. Blocked IP wins over allowed IP when both apply.
5. User network policy has priority over account policy for that user.
6. Masking = columns; Row Access Policy = rows.
7. Trust Center is for security posture, not ordinary usage history.
8. Resource Monitor focuses on warehouse credits; it is not a general storage-cost monitor.
