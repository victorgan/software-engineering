# Leftmost Prefix Rule

> <- Back to [[Composite Indexes]]

A composite index on columns (A, B, C) can be used for queries filtering on A, (A, B), or (A, B, C) but not on B alone or (B, C). The index is only effective for leftmost prefixes of the column list.

#relational-databases #indexing #composite
