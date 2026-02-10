# Livelock

> <- Back to [[Deadlocks & Livelocks]]

A situation where threads are actively executing but making no progress, like two people in a hallway who keep stepping aside for each other in the same direction. Unlike deadlock, threads are not blocked — they are busy but unproductive. Adding randomized backoff can resolve livelocks.

## Key Properties

- [[Actively Changing State But No Progress]]

---

#concurrency #livelock
