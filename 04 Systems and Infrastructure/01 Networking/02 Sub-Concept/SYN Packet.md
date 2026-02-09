# SYN Packet

> <- Back to [[Three-Way Handshake]]

The initial packet sent by the client to begin a TCP connection. Contains the client's initial sequence number (ISN) and the SYN flag set. SYN flood attacks exploit this by sending many SYN packets without completing the handshake, exhausting server resources. SYN cookies mitigate this.

#networking #tcp
