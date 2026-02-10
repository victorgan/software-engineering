# Keep-Alive Default

> <- Back to [[HTTP 1.1]]

HTTP/1.1 keeps TCP connections open by default (Connection: keep-alive), unlike HTTP/1.0 which closed connections after each response. This eliminates the cost of repeated TCP handshakes and slow start for subsequent requests to the same server.

#networking #http #performance
