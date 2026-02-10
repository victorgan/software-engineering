# Sequential Key Problems

> <- Back to [[Range-Based Partitioning]]

Auto-incrementing IDs or timestamps as partition keys create hotspots because all new writes go to the same partition (the one handling the highest key range). Solutions: random prefixes, reverse timestamps, or switching to hash-based partitioning for the write-heavy portion.

#distributed-systems #sharding
