# HTTP Upgrade Handshake

> <- Back to [[WebSockets]]

WebSocket connections begin as an HTTP/1.1 request with an Upgrade: websocket header. The server responds with 101 Switching Protocols, and the connection switches from HTTP to the WebSocket protocol. This reuse of HTTP for the initial handshake makes WebSockets compatible with existing infrastructure.

#networking #websockets
