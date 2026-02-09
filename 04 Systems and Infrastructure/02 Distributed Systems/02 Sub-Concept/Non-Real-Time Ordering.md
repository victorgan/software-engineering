# Non-Real-Time Ordering

> <- Back to [[Sequential Consistency]]

Unlike linearizability, sequential consistency does not require the global order to respect real-time (wall-clock) ordering. An operation that completes before another starts might appear later in the sequential order. This relaxation is what makes it weaker than linearizability but easier to implement.

#distributed-systems #consistency
