# Threads vs Processes

> <- Back to [[Fundamentals]]

Processes have isolated memory spaces and communicate via IPC (pipes, sockets, shared memory), providing strong isolation at higher overhead. Threads share memory within a process, are lighter weight to create and switch, but require synchronization to avoid data races.

## Key Properties

- [[Shared Memory vs Isolated Memory]]
- [[Lighter vs Heavier Weight]]

---

#concurrency #threads #processes
