# Chunked Transfer

> <- Back to [[HTTP 1.1]]

Transfer-Encoding: chunked allows the server to start sending a response before knowing its total size. Data is sent in chunks, each prefixed with its size in hexadecimal. Enables streaming responses and server-sent events. A zero-length chunk signals the end.

#networking #http
