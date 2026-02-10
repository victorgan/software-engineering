# Flash Attention

> <- Back to [[Transformers]]

An IO-aware exact attention algorithm that reduces memory usage from O(n^2) to O(n) and significantly speeds up training. Achieves this by tiling the attention computation to minimize reads/writes to GPU high-bandwidth memory (HBM). Now standard in modern Transformer training.

## Related

- [[Self-Attention]] (what Flash Attention optimizes)
- [[Mixed Precision Training]] (complementary optimization)

---

#deep-learning #transformers #flash-attention #optimization
