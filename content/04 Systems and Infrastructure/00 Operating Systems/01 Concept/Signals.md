# Signals

> <- Back to [[Linux Internals]]

Asynchronous notifications sent to processes to indicate events. SIGTERM requests graceful shutdown, SIGKILL forces immediate termination (cannot be caught), SIGHUP traditionally triggers config reload. Signal handlers allow processes to define custom responses. Critical for process lifecycle management.

## Key Properties

- [[SIGTERM and SIGKILL]]
- [[Signal Handlers]]
- [[SIGHUP Reload]]

## Related

- [[Process Lifecycle]] (signals trigger state transitions)
- [[systemd]] (uses signals to manage services)
- [[Signals IPC]] (signals as an IPC mechanism)

---

#operating-systems #linux #signals
