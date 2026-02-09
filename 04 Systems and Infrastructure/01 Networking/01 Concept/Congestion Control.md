# Congestion Control

> <- Back to [[TCP Deep Dive]]

Algorithms that prevent the sender from overwhelming the network. Starts with slow start (exponential growth), transitions to congestion avoidance (linear growth), and reduces the sending rate on packet loss. Different algorithms (Reno, Cubic, BBR) use different signals and strategies.

## Key Properties

- [[Slow Start]]
- [[Congestion Avoidance]]
- [[Fast Retransmit]]
- [[BBR Algorithm]]

## Related

- [[Flow Control]] (prevents overwhelming the receiver)
- [[Backpressure]] (application-level congestion management)

---

#networking #tcp #performance
