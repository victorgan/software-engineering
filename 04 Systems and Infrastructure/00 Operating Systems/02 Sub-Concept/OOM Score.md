# OOM Score

> <- Back to [[OOM Killer]]

A score (0-1000) assigned to each process by the Linux kernel indicating how likely it is to be killed when memory runs out. Based on memory usage, process age, and other heuristics. Can be adjusted via /proc/pid/oom_score_adj to protect critical processes (e.g., set to -1000 for unkillable).

#operating-systems #memory #linux
