# Fast Retransmit

> <- Back to [[Congestion Control]]

When the sender receives three duplicate ACKs for the same segment, it retransmits the missing segment immediately without waiting for the retransmission timeout. This is faster than waiting for the timeout (which can be seconds). Combined with fast recovery to avoid returning to slow start.

#networking #tcp
