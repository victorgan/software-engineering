# Actively Changing State But No Progress

> <- Back to [[Livelock]]

Unlike deadlocked threads which are blocked, livelocked threads are actively running — they keep responding to each other's actions but never actually advance their work. Adding randomized delays or backoff jitter can break the cycle and allow progress.

#concurrency #livelock #no-progress
