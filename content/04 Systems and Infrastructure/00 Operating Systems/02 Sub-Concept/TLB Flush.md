# TLB Flush

> <- Back to [[Context Switching]]

When switching between processes, the Translation Lookaside Buffer (TLB) — a cache of virtual-to-physical address mappings — must be flushed since each process has its own address space. This is a major source of context switch overhead. Thread switches within the same process avoid this cost.

#operating-systems #context-switching #memory
