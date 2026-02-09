# Async IO

> <- Back to [[IO Models]]

True asynchronous I/O where the application submits operations and is notified upon completion without any blocking or polling. Linux's io_uring (since kernel 5.1) provides high-performance async I/O with a shared ring buffer between user and kernel space, supporting batched submissions and completions.

#operating-systems #io #performance
