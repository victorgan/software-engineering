# CSP (Communicating Sequential Processes)

> <- Back to [[Concurrency Models]]

A model where concurrent processes communicate through typed channels. Unlike actors, channels are synchronization points — a send blocks until a receiver is ready (or channels can be buffered). Go's goroutines and channels are the most prominent CSP implementation.

## Key Properties

- [[Channels as Synchronization Points]]
- [[Goroutines and core.async]]

---

#concurrency #models #csp
