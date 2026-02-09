# Overcommit Settings

> <- Back to [[OOM Killer]]

Linux can allocate more virtual memory than physical RAM available (overcommit), betting that not all processes will use their full allocation simultaneously. Controlled via vm.overcommit_memory sysctl (0=heuristic, 1=always allow, 2=never overcommit). Overcommit makes OOM situations possible.

#operating-systems #memory #linux
