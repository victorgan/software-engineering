# Zero-RTT Setup

> <- Back to [[HTTP 3]]

QUIC supports 0-RTT connection resumption — the client can send application data in the very first packet when reconnecting to a previously visited server. This eliminates the 1-2 RTT overhead of TCP handshake + TLS handshake, dramatically improving latency for repeat connections.

#networking #http #quic #performance
