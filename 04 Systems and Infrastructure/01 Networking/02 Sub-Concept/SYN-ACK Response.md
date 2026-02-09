# SYN-ACK Response

> <- Back to [[Three-Way Handshake]]

The server's response to a SYN, containing both the SYN flag (with the server's initial sequence number) and an ACK of the client's SYN. The server allocates connection state at this point, which is why SYN floods are effective — they force the server to allocate resources for half-open connections.

#networking #tcp
