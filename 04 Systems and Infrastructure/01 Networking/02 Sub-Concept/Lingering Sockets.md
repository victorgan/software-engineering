# Lingering Sockets

> <- Back to [[Connection Termination]]

Sockets stuck in TIME_WAIT or CLOSE_WAIT states that consume port numbers and file descriptors. High connection rates can exhaust available ports. Mitigations include SO_REUSEADDR, SO_REUSEPORT, reducing TIME_WAIT duration (tcp_fin_timeout), and connection pooling.

#networking #tcp
