# Fragmentation Concerns

> <- Back to [[Heap Memory]]

Over time, heap allocations and deallocations create gaps of free memory between allocated blocks. External fragmentation means sufficient total free memory exists but not in contiguous blocks. Compacting GCs and slab allocators are strategies to mitigate fragmentation.

#memory-models #heap #fragmentation
