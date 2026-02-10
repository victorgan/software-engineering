# Data Parallelism

> <- Back to [[Training at Scale]]

Replicate the entire model on each GPU; split the training data across GPUs. Each GPU computes gradients on its data shard, then gradients are synchronized (all-reduce). The simplest and most common form of distributed training.

## Related

- [[Model Parallelism]] (split the model instead)
- [[Gradient Accumulation]] (simulate larger batches)

---

#deep-learning #distributed-training #data-parallelism
