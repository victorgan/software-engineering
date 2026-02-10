# Fork-Join

> <- Back to [[Data Parallelism]]

A parallel execution pattern where a task recursively splits (forks) into smaller subtasks until they are small enough to execute sequentially, then combines (joins) the results. Work stealing balances load across threads.

## Key Properties

- [[Recursive Task Decomposition]]
- [[Work Stealing]]

## Related

- Java ForkJoinPool

---

#concurrency #data-parallelism #fork-join
