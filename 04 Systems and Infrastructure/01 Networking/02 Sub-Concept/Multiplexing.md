# Multiplexing

> <- Back to [[HTTP 2]]

Multiple HTTP request-response exchanges (streams) interleaved on a single TCP connection. Each stream has a unique ID and can be prioritized. Eliminates HTTP-level head-of-line blocking — a slow response on one stream does not block others. Dramatically reduces the need for multiple connections.

#networking #http #performance
