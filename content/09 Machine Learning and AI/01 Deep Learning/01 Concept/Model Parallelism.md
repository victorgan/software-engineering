# Model Parallelism

> <- Back to [[Training at Scale]]

Split the model across multiple GPUs when it is too large to fit on a single device. Two main types: tensor parallelism (split individual layers across GPUs) and pipeline parallelism (assign different layers to different GPUs).

## Related

- [[Data Parallelism]] (split data instead of model)
- [[Distributed Training Frameworks]] (implement model parallelism)

---

#deep-learning #distributed-training #model-parallelism
