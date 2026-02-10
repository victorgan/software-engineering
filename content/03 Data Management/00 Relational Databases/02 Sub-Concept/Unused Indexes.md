# Unused Indexes

> <- Back to [[Index Anti-Patterns]]

Indexes that exist but are never used by the query planner. They consume storage and slow down writes with no read benefit. Identify with pg_stat_user_indexes or similar tools.

#relational-databases #indexing #anti-patterns
