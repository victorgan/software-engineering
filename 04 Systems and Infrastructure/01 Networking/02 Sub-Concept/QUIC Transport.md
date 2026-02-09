# QUIC Transport

> <- Back to [[HTTP 3]]

HTTP/3 uses QUIC as its transport layer instead of TCP. QUIC runs over UDP with built-in TLS 1.3, providing encryption by default. Stream-level flow control means packet loss on one stream does not affect others, solving the TCP head-of-line blocking problem that limited HTTP/2.

#networking #http #quic
