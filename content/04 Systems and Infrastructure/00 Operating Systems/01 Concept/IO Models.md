# IO Models

> <- Back to [[File Systems]]

Different approaches to handling I/O operations. Blocking I/O waits for completion; non-blocking returns immediately. I/O multiplexing (select, poll, epoll, kqueue) monitors multiple file descriptors efficiently. Async I/O (io_uring) submits operations and gets notified on completion.

## Key Properties

- [[Blocking and Non-Blocking IO]]
- [[IO Multiplexing]]
- [[Async IO]]

## Related

- [[Coroutines]] (often built on non-blocking I/O)
- [[Green Threads and Fibers]] (runtime manages I/O scheduling)

---

#operating-systems #file-systems #io
