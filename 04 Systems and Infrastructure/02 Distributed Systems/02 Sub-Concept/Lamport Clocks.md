# Lamport Clocks

> <- Back to [[Distributed Time]]

A logical clock that provides a partial ordering of events. Each node maintains a counter incremented on local events and message sends; on message receipt, the counter is set to max(local, received) + 1. If event A causally precedes event B, then L(A) < L(B), but the converse is not necessarily true.

#distributed-systems #time
