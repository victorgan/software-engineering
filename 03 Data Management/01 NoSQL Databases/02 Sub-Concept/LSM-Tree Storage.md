# LSM-Tree Storage

> <- Back to [[Column-Family Store Concept]]

Log-Structured Merge-Tree. Writes go to an in-memory buffer (memtable), then flush to sorted immutable files (SSTables) on disk. Background compaction merges SSTables. Optimizes write throughput at the cost of read amplification.

#nosql #column-family #lsm-tree
