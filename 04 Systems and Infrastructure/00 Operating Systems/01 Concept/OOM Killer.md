# OOM Killer

> <- Back to [[Memory Management]]

The Linux kernel's out-of-memory handler that selects and kills processes when the system runs out of memory. It scores processes based on memory usage, age, and other factors. In containerized environments, cgroups memory limits trigger OOM kills at the container level.

## Key Properties

- [[OOM Score]]
- [[cgroups Memory Limits]]
- [[Overcommit Settings]]

## Related

- [[Virtual Memory]] (overcommit can defer OOM situations)
- [[cgroups]] (container-level memory limits)

---

#operating-systems #memory #linux
