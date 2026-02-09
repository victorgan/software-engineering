# OTP Supervision Trees

> <- Back to [[Erlang-Elixir Concurrency]]

A hierarchical structure where supervisor processes monitor worker processes. When a worker crashes, its supervisor restarts it according to a configured strategy (one-for-one, one-for-all, rest-for-one). This "let it crash" philosophy provides fault tolerance through isolation and automatic recovery.

#concurrency #language-specific #erlang #elixir #otp #supervision
