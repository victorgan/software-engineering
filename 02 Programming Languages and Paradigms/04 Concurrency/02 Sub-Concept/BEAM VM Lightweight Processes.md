# BEAM VM Lightweight Processes

> <- Back to [[Erlang-Elixir Concurrency]]

The BEAM virtual machine supports millions of lightweight, isolated processes with tiny initial stacks (~300 bytes). Processes are preemptively scheduled (reduction counting), share nothing, and communicate via message passing. Process creation takes microseconds.

#concurrency #language-specific #erlang #elixir #beam
