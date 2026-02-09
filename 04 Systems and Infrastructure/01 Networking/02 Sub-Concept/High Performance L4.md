# High Performance L4

> <- Back to [[Layer 4 Load Balancing]]

L4 load balancers can handle millions of connections per second with minimal CPU usage since they do not need to parse application-layer protocols. Some implementations use kernel bypass (DPDK, XDP/eBPF) for even higher performance. Ideal for non-HTTP protocols and high-throughput scenarios.

#networking #load-balancing #performance
