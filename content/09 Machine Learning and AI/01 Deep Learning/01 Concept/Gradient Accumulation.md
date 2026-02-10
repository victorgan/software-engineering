# Gradient Accumulation

> <- Back to [[Training at Scale]]

Simulate larger batch sizes by accumulating gradients over multiple forward/backward passes before performing a weight update. Enables effective large-batch training on limited GPU memory.

## Related

- [[Data Parallelism]] (alternative way to increase effective batch size)
- [[Mixed Precision Training]] (complementary memory optimization)

---

#deep-learning #distributed-training #gradient-accumulation
