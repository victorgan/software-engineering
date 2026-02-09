# Memory Limits

> <- Back to [[cgroups]]

cgroups enforce hard memory limits (memory.max in v2) for process groups. When a cgroup exceeds its limit, the OOM killer targets processes within that cgroup. In Kubernetes, memory limits map to cgroup memory controls. Unlike CPU throttling, exceeding memory limits kills the process.

#operating-systems #linux #containers
