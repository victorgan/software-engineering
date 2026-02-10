# Single-threaded Event Loop

> <- Back to [[JavaScript Concurrency]]

JavaScript executes on a single thread with an event loop that processes callbacks from a queue. I/O operations are delegated to the runtime (libuv in Node.js, browser APIs), and their callbacks are queued for execution. This simplifies programming but means CPU-intensive work blocks the entire loop.

#concurrency #language-specific #javascript #event-loop
