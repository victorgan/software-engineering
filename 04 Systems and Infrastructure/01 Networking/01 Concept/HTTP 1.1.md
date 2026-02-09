# HTTP 1.1

> <- Back to [[HTTP]]

The first widely-adopted HTTP version with persistent connections (keep-alive) by default. Supports pipelining (sending multiple requests without waiting for responses) and chunked transfer encoding for streaming. Limited by head-of-line blocking — one slow response blocks all subsequent responses on that connection.

## Key Properties

- [[Keep-Alive Default]]
- [[Pipelining]]
- [[Chunked Transfer]]

## Related

- [[HTTP 2]] (addresses head-of-line blocking with multiplexing)
- [[Keep-Alive]] (TCP-level persistent connections)

---

#networking #http
