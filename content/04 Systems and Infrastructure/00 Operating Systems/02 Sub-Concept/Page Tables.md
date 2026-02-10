# Page Tables

> <- Back to [[Virtual Memory]]

Data structures maintained by the OS that map virtual page numbers to physical frame numbers. Modern systems use multi-level page tables (4-level on x86-64) to reduce memory overhead. Each process has its own page table, switched during context switches.

#operating-systems #memory #virtual-memory
