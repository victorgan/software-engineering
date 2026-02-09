# Kernel vs User Space

> <- Back to [[Memory Management]]

The fundamental privilege separation in operating systems. Kernel space has full hardware access and runs OS code; user space runs application code with restricted privileges. System calls are the interface between them, requiring a mode switch that has measurable overhead.

## Key Properties

- [[Privilege Levels]]
- [[System Calls]]
- [[Mode Switching]]

## Related

- [[Virtual Memory]] (enforces the kernel/user boundary)
- [[eBPF]] (safely runs user code in kernel space)

---

#operating-systems #memory #security
