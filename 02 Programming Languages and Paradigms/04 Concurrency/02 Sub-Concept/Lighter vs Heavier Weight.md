# Lighter vs Heavier Weight

> <- Back to [[Threads vs Processes]]

Thread creation and context switching is faster than process creation because threads share the same address space, page tables, and file descriptors. Processes require copying or creating new address spaces (though fork + copy-on-write mitigates this).

#concurrency #threads #processes #overhead
