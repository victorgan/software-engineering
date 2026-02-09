# Lightweight Execution

> <- Back to [[Thread]]

Threads are cheaper to create and destroy than processes because they share the parent process's address space and resources. Context switching between threads is faster since there is no need to switch memory mappings or flush the TLB.

#operating-systems #threads #performance
