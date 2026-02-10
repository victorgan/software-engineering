# Timeouts

> <- Back to [[Reliability Patterns]]

Always set timeouts on external calls to prevent indefinite blocking. Adaptive timeouts adjust based on observed latency. Without timeouts, a slow dependency can exhaust thread pools and cascade failure through the entire system.

## Key Properties

- [[Timeout Configuration]]
- [[Adaptive Timeouts]]
- [[Timeout vs Retry Interaction]]

---

#sre #reliability #timeouts
