# Mixture of Experts

> <- Back to [[Transformers]]

A sparse architecture where only a subset of parameters (experts) are activated for each input token. A gating network routes tokens to the appropriate experts. Enables much larger models without proportional increase in compute. Used in Mixtral, Switch Transformer, and reportedly in GPT-4.

## Related

- [[Scaling Laws]] (MoE changes compute-performance tradeoff)
- [[Model Parallelism]] (experts can be distributed across GPUs)

---

#deep-learning #transformers #moe #sparse
