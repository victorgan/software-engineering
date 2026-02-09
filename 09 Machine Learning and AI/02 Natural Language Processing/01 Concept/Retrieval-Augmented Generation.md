# Retrieval-Augmented Generation

> <- Back to [[Large Language Models]]

Enhance LLM responses by retrieving relevant documents and injecting them into the context. Reduces hallucination, enables access to private/recent data, and provides attributable answers.

## Key Properties

- [[Vector Databases]]
- [[Embedding Models]]
- [[Chunking Strategies]]
- [[Retrieval Methods]]

## Architecture

1. User query -> embed query
2. Search vector database for similar documents
3. Inject retrieved documents into LLM prompt
4. LLM generates answer grounded in retrieved context

## Related

- [[Embeddings]] (encode documents and queries)
- [[Foundation Models]] (generate answers from context)

---

#nlp #llm #rag #retrieval
