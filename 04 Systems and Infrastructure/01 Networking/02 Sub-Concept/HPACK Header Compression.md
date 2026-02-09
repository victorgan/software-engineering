# HPACK Header Compression

> <- Back to [[HTTP 2]]

A header compression algorithm specific to HTTP/2 that uses Huffman encoding and a dynamic table of previously seen headers. Dramatically reduces header overhead, especially for repeated requests with similar headers (cookies, user-agent, etc.). Designed to be resistant to CRIME-style compression attacks.

#networking #http #performance
