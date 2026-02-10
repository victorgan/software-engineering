# Multilevel Feedback Queue

> <- Back to [[Scheduling Algorithms]]

Multiple queues with different priorities and time quanta. Processes move between queues based on behavior: CPU-bound processes sink to lower-priority queues with larger quanta, while I/O-bound processes stay in higher-priority queues. Used by most modern OS schedulers (Linux CFS is a variant).

#operating-systems #scheduling #algorithms
