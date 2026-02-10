# Flow Control

> <- Back to [[TCP Deep Dive]]

Prevents a fast sender from overwhelming a slow receiver. The receiver advertises a window size indicating how much data it can buffer. The sender must not send more than this window. Uses a sliding window protocol to efficiently utilize the link while respecting receiver capacity.

## Key Properties

- [[Sliding Window]]
- [[Receiver Window]]
- [[Window Scaling]]

## Related

- [[Congestion Control]] (prevents overwhelming the network, not just receiver)
- [[Backpressure]] (application-level flow control)

---

#networking #tcp
