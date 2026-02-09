# Fine-Tuning LLMs

> <- Back to [[Large Language Models]]

Adapting a pretrained LLM to specific tasks or domains by further training on task-specific data. Ranges from full fine-tuning to parameter-efficient methods.

## Methods

- **Full Fine-Tuning** -- update all weights, expensive but most capable
- **LoRA (Low-Rank Adaptation)** -- add small trainable matrices, freeze original weights
- **QLoRA** -- LoRA on quantized models, enables fine-tuning on consumer GPUs
- **Adapter Methods** -- insert small trainable modules between frozen layers

## Related

- [[Foundation Models]] (starting point for fine-tuning)
- [[RLHF and Alignment]] (fine-tuning for alignment)

---

#nlp #llm #fine-tuning #lora
