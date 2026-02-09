# Connection Termination

> <- Back to [[TCP Deep Dive]]

Graceful connection close using a four-way handshake: initiator sends FIN, receiver ACKs, receiver sends FIN, initiator ACKs. The initiator enters TIME_WAIT state for 2*MSL (typically 60 seconds) to handle delayed packets. Lingering sockets in TIME_WAIT can exhaust port space on busy servers.

## Key Properties

- [[FIN Handshake]]
- [[TIME_WAIT State]]
- [[Lingering Sockets]]

## Related

- [[Three-Way Handshake]] (opening the connection)
- [[Keep-Alive]] (avoiding connection teardown/setup overhead)

---

#networking #tcp
