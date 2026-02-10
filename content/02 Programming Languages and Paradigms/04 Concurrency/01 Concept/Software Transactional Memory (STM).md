# Software Transactional Memory (STM)

> <- Back to [[Concurrency Models]]

An approach where shared memory operations are grouped into transactions that appear to execute atomically. If a conflict is detected (another transaction modified the same data), the transaction is automatically retried. Eliminates manual lock management.

## Key Properties

- [[Transactions on Shared Memory]]
- [[Automatic Retry on Conflict]]

## Related

- Haskell, Clojure

---

#concurrency #models #stm
