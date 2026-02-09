# Circuit States

> <- Back to [[Circuit Breaker]]

Closed: requests flow normally, failures are counted. Open: requests are immediately rejected without calling the service (fail fast). Half-Open: after a timeout, a limited number of test requests are allowed through — if they succeed, the circuit closes; if they fail, it reopens.

#distributed-systems #patterns #resilience
