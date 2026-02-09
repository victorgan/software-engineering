# Namespaces

> <- Back to [[Linux Internals]]

Linux kernel feature that isolates system resources for groups of processes. Each namespace type provides a separate view: PID (process IDs), network (network stack), mount (filesystem mounts), user (user/group IDs), UTS (hostname), and IPC. Namespaces are the foundation of container isolation.

## Key Properties

- [[PID Namespace]]
- [[Network Namespace]]
- [[Mount Namespace]]
- [[User Namespace]]

## Related

- [[cgroups]] (resource limits — the other pillar of containers)
- [[Docker]] (uses namespaces for container isolation)

---

#operating-systems #linux #containers
