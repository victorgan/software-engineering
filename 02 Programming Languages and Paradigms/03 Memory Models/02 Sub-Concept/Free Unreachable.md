# Free Unreachable

> <- Back to [[Mark-and-Sweep]]

The sweep phase iterates through all allocated objects and reclaims those not marked as reachable. The freed memory is returned to the free list for future allocations. Unlike reference counting, mark-and-sweep naturally handles circular references.

#memory-models #gc #sweep #free
