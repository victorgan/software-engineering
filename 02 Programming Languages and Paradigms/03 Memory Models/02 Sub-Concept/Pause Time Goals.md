# Pause Time Goals

> <- Back to [[GC Tuning]]

Specifying the maximum acceptable GC pause duration. The collector adjusts its behavior (collection frequency, region sizes) to meet the target. G1's `-XX:MaxGCPauseMillis` and ZGC's sub-millisecond goals exemplify configurable pause time targets.

#memory-models #gc #tuning #pause-time
