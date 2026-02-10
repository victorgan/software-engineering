# Memory-Mapped Files (OS)

> <- Back to [[Memory Management]]

Files mapped directly into a process's virtual address space using mmap. Enables zero-copy I/O — reading and writing files as if they were arrays in memory. The OS handles paging file contents in and out of RAM transparently.

## Key Properties

- [[mmap System Call]]
- [[Zero-Copy IO]]
- [[Lazy Loading]]

## Related

- [[Virtual Memory]] (memory-mapped files leverage the VM system)
- [[Paging]] (file pages are demand-loaded like regular pages)

---

#operating-systems #memory #io
