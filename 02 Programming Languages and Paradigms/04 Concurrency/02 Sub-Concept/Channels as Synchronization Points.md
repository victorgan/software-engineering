# Channels as Synchronization Points

> <- Back to [[CSP (Communicating Sequential Processes)]]

Channels are typed conduits through which goroutines (or processes) send and receive values. Unbuffered channels synchronize sender and receiver (both block until the other is ready). Buffered channels decouple sender and receiver up to the buffer capacity.

#concurrency #models #csp #channels
