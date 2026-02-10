# TIME_WAIT State

> <- Back to [[Connection Termination]]

After sending the final ACK, the initiating side enters TIME_WAIT for 2*MSL (Maximum Segment Lifetime, typically 60 seconds). This ensures delayed packets from the old connection are not confused with a new connection on the same port. Can cause port exhaustion on busy servers with many short-lived connections.

#networking #tcp
