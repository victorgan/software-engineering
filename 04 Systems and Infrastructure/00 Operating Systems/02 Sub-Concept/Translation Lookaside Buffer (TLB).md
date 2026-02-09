# Translation Lookaside Buffer (TLB)

> <- Back to [[Virtual Memory]]

A hardware cache of recent virtual-to-physical address translations. TLB hits avoid the expensive multi-level page table walk. TLB misses are costly (tens to hundreds of cycles). TLB entries must be flushed on process context switches since each process has different mappings.

#operating-systems #memory #virtual-memory #performance
