# Avoid Table Lookups

> <- Back to [[Covering Indexes]]

When a covering index contains all necessary columns, the database avoids the expensive step of fetching the full row from the heap/table, significantly improving query performance.

#relational-databases #indexing #covering
