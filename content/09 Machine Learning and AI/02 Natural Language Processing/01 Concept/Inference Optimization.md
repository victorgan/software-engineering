# Inference Optimization

> <- Back to [[Large Language Models]]

Techniques for making LLM inference faster, cheaper, and more memory-efficient in production.

## Key Techniques

- **Quantization** -- reduce weight precision (INT8, INT4) with minimal quality loss
- **KV-Cache** -- cache key/value matrices across tokens to avoid recomputation
- **Speculative Decoding** -- use small model to draft, large model to verify
- **vLLM** -- efficient inference engine with PagedAttention for memory management
- **Continuous Batching** -- process multiple requests efficiently

## Related

- [[Model Serving]] (production deployment)
- [[Mixed Precision Training]] (related precision techniques)

---

#nlp #llm #inference #optimization
