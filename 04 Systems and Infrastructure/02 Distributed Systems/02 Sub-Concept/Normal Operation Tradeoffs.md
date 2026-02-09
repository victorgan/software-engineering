# Normal Operation Tradeoffs

> <- Back to [[PACELC Theorem]]

PACELC reveals that systems classified the same under CAP (e.g., both AP) can behave differently during normal operation. Dynamo (PA/EL) trades consistency for latency in both cases. PAXOS-based systems (PC/EC) prioritize consistency always. Understanding both dimensions is key to choosing the right system.

#distributed-systems #fundamentals
