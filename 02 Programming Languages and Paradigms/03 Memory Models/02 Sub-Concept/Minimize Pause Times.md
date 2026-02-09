# Minimize Pause Times

> <- Back to [[Concurrent GC]]

Concurrent GCs perform marking, sweeping, and compaction alongside application threads rather than stopping the world. This reduces GC pauses from seconds to milliseconds or less, critical for latency-sensitive applications like trading systems and real-time services.

#memory-models #gc #concurrent #pause-times
