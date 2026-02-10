# Signal Handlers

> <- Back to [[Signals]]

Functions registered by a process to execute when a specific signal is received. Handlers allow graceful shutdown (SIGTERM), config reload (SIGHUP), or custom behavior. Signal handlers run asynchronously and must be async-signal-safe — only certain functions can be safely called from handlers.

#operating-systems #linux #signals
