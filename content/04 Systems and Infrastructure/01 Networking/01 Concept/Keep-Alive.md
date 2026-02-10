# Keep-Alive

> <- Back to [[TCP Deep Dive]]

Persistent TCP connections that remain open for multiple request-response exchanges, avoiding the overhead of repeated handshakes and slow start. HTTP/1.1 uses keep-alive by default. Connection pooling reuses established connections across requests. Idle connections are periodically probed to detect failures.

## Key Properties

- [[Persistent Connections]]
- [[Connection Pooling]]
- [[Idle Timeout]]

## Related

- [[Three-Way Handshake]] (overhead that keep-alive avoids)
- [[HTTP 1.1]] (keep-alive is default in HTTP/1.1)

---

#networking #tcp #performance
