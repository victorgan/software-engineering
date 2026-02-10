# HTTP 3

> <- Back to [[HTTP]]

Built on QUIC (UDP-based transport) instead of TCP. Eliminates TCP-level head-of-line blocking — a lost packet only affects its stream, not others. Provides 0-RTT connection setup, built-in encryption (TLS 1.3), and connection migration when network changes (e.g., Wi-Fi to cellular).

## Key Properties

- [[QUIC Transport]]
- [[Zero-RTT Setup]]
- [[Connection Migration]]

## Related

- [[HTTP 2]] (predecessor, TCP-based)
- [[QUIC Protocol]] (underlying transport)

---

#networking #http
