# SIGTERM and SIGKILL

> <- Back to [[Signals]]

SIGTERM (15) requests graceful shutdown — the process can catch it and clean up before exiting. SIGKILL (9) immediately terminates the process — it cannot be caught, blocked, or ignored. Kubernetes sends SIGTERM first, waits a grace period, then sends SIGKILL.

#operating-systems #linux #signals
