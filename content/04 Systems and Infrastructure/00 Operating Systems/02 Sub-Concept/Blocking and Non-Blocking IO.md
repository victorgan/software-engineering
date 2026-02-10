# Blocking and Non-Blocking IO

> <- Back to [[IO Models]]

Blocking I/O suspends the calling thread until the operation completes — simple but wastes CPU time waiting. Non-blocking I/O returns immediately with EAGAIN/EWOULDBLOCK if data is not ready, requiring the application to poll or use event notification. Non-blocking is the foundation of high-performance servers.

#operating-systems #io
