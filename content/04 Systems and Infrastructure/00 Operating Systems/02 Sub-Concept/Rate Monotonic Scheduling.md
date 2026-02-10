# Rate Monotonic Scheduling

> <- Back to [[Real-Time Scheduling]]

A static-priority preemptive algorithm where tasks with shorter periods (higher rates) get higher priorities. Optimal among fixed-priority algorithms. Can guarantee schedulability if total CPU utilization is below ~69% (for n tasks, the bound is n(2^(1/n) - 1)).

#operating-systems #scheduling #real-time
