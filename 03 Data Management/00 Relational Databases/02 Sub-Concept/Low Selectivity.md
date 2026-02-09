# Low Selectivity

> <- Back to [[Index Anti-Patterns]]

Indexing columns with few distinct values (e.g., boolean, status with 3 values). The query planner often ignores such indexes in favor of sequential scans because most rows match.

#relational-databases #indexing #anti-patterns
