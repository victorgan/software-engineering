# Self-Attention

> <- Back to [[Transformers]]

The core mechanism of Transformers. Each position attends to all other positions, computing attention scores from Query, Key, and Value matrices. Attention(Q,K,V) = softmax(QK^T / sqrt(d_k)) * V. Enables capturing long-range dependencies in O(1) layers.

## Related

- [[Multi-Head Attention]] (parallel attention heads)
- [[Flash Attention]] (efficient implementation)

---

#deep-learning #transformers #attention
