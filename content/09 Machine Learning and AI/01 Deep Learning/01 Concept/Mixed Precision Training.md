# Mixed Precision Training

> <- Back to [[Training at Scale]]

Use lower precision (FP16 or BF16) for most computations while keeping FP32 master weights. Roughly doubles training speed and halves memory usage with minimal accuracy loss. BF16 preferred for its wider dynamic range. Now standard practice.

## Related

- [[Flash Attention]] (complementary optimization)
- [[Gradient Accumulation]] (both reduce memory pressure)

---

#deep-learning #distributed-training #mixed-precision
