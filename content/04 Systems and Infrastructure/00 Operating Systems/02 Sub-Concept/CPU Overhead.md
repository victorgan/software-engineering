# CPU Overhead

> <- Back to [[Context Switching]]

Context switches consume CPU cycles for saving/restoring state and flushing caches. Typical cost is 1-10 microseconds. Excessive context switching (thrashing) degrades performance. Thread switches are cheaper than process switches since they share the address space.

#operating-systems #context-switching #performance
