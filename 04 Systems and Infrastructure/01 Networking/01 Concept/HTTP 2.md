# HTTP 2

> <- Back to [[HTTP]]

Major revision that introduces multiplexing (multiple concurrent streams over a single TCP connection), HPACK header compression, server push, and binary framing. Eliminates HTTP-level head-of-line blocking but still suffers from TCP-level head-of-line blocking when packets are lost.

## Key Properties

- [[Multiplexing]]
- [[HPACK Header Compression]]
- [[Server Push]]

## Related

- [[HTTP 1.1]] (predecessor)
- [[HTTP 3]] (addresses TCP-level head-of-line blocking)

---

#networking #http
