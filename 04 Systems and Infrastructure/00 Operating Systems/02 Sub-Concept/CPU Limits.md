# CPU Limits

> <- Back to [[cgroups]]

cgroups can limit CPU usage via cpu.shares (relative weight), cpu.cfs_quota_us/cpu.cfs_period_us (hard limits), and cpuset (pin to specific cores). In Kubernetes, CPU requests and limits map directly to cgroup CPU controls. Throttling occurs when a container exceeds its CPU quota.

#operating-systems #linux #containers
