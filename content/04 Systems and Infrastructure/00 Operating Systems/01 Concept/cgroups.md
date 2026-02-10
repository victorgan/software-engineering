# cgroups

> <- Back to [[Linux Internals]]

Control groups — a Linux kernel feature for limiting, accounting, and isolating resource usage (CPU, memory, I/O, network) of process groups. Combined with namespaces, cgroups form the foundation of container technology. cgroups v2 provides a unified hierarchy and improved resource management.

## Key Properties

- [[CPU Limits]]
- [[Memory Limits]]
- [[IO Limits]]

## Related

- [[Namespaces]] (isolation — the other pillar of containers)
- [[OOM Killer]] (triggered when cgroup memory limit is exceeded)
- [[Docker]] (uses cgroups for resource limits)

---

#operating-systems #linux #containers
