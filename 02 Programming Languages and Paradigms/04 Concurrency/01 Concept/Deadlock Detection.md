# Deadlock Detection

> <- Back to [[Deadlocks & Livelocks]]

Detecting deadlocks after they occur rather than preventing them. Wait-for graphs track which threads are waiting on which resources; a cycle in this graph indicates deadlock. The system can then recover by killing a thread or releasing resources.

## Key Properties

- [[Wait-for Graphs]]
- [[Cycle Detection (Deadlock)]]

---

#concurrency #deadlock #detection
