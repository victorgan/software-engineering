# FIN Handshake

> <- Back to [[Connection Termination]]

A four-step process to gracefully close a TCP connection. Either side can initiate by sending FIN. The other side ACKs the FIN, then sends its own FIN when ready, which is also ACKed. This allows both sides to finish sending pending data before closing.

#networking #tcp
