# IO Multiplexing

> <- Back to [[IO Models]]

Monitoring multiple file descriptors simultaneously to determine which are ready for I/O. select() is portable but O(n); poll() removes the fd limit; epoll (Linux) and kqueue (BSD/macOS) provide O(1) event notification and scale to millions of connections. The basis of event-driven servers like Nginx and Node.js.

#operating-systems #io #networking
