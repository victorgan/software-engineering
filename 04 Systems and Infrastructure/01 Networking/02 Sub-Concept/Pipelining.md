# Pipelining

> <- Back to [[HTTP 1.1]]

Sending multiple HTTP requests on the same connection without waiting for each response. Rarely used in practice because responses must be returned in order (head-of-line blocking), and many servers and proxies do not support it properly. HTTP/2 multiplexing supersedes pipelining.

#networking #http
