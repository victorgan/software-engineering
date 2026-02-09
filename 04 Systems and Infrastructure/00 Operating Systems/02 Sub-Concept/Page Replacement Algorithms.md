# Page Replacement Algorithms

> <- Back to [[Paging]]

When physical memory is full and a new page must be loaded, the OS must choose a page to evict. LRU (Least Recently Used) is theoretically good but expensive to implement exactly. The Clock algorithm approximates LRU efficiently. Linux uses a two-list approach (active/inactive lists).

#operating-systems #memory #paging #algorithms
