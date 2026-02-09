# Sliding Window

> <- Back to [[Flow Control]]

A mechanism that allows the sender to have multiple unacknowledged packets in flight. The window "slides" forward as acknowledgments arrive, enabling efficient use of the link. Window size determines throughput: throughput = window_size / RTT.

#networking #tcp #performance
