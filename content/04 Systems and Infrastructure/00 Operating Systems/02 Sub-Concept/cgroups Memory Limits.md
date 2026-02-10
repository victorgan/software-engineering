# cgroups Memory Limits

> <- Back to [[OOM Killer]]

Control groups allow setting hard memory limits for a group of processes (used heavily in containers). When a cgroup exceeds its memory limit, the OOM killer targets processes within that cgroup rather than the system-wide OOM killer activating. This provides container-level isolation.

#operating-systems #memory #linux #containers
