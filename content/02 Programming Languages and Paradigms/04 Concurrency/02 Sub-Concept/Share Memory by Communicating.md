# Share Memory by Communicating

> <- Back to [[Go Concurrency]]

Go's concurrency philosophy: instead of protecting shared data with locks, pass data between goroutines through channels. When data is sent on a channel, ownership is conceptually transferred to the receiver, avoiding the need for explicit synchronization.

#concurrency #language-specific #go #philosophy
