# Three-Way Handshake

> <- Back to [[TCP Deep Dive]]

The process of establishing a TCP connection. Client sends SYN (synchronize), server responds with SYN-ACK, client completes with ACK. This exchanges initial sequence numbers and establishes connection state on both sides. Takes one round-trip time (RTT) before data can flow.

## Key Properties

- [[SYN Packet]]
- [[SYN-ACK Response]]
- [[ACK Completion]]

## Related

- [[Connection Termination]] (closing the connection)
- [[Keep-Alive]] (avoiding repeated handshakes)

---

#networking #tcp
