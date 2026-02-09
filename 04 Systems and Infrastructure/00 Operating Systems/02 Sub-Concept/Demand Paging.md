# Demand Paging

> <- Back to [[Paging]]

Pages are loaded into physical memory only when first accessed, not when the process starts. This reduces memory usage and startup time since most programs never touch all their pages. Combined with copy-on-write, this makes fork() efficient.

#operating-systems #memory #paging
