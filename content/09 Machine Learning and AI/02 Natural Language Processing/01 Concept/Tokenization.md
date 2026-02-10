# Tokenization

> <- Back to [[Text Processing Pipeline]]

Breaking text into tokens (the atomic units the model processes). The tokenization strategy directly affects vocabulary size, handling of rare words, and model performance.

## Key Methods

- **Word-level** -- split on whitespace/punctuation, large vocabulary, OOV problem
- **Subword (BPE)** -- Byte-Pair Encoding, merge frequent character pairs, used in GPT
- **WordPiece** -- similar to BPE, used in BERT
- **SentencePiece** -- language-agnostic, treats text as raw bytes, used in LLaMA
- **Unigram** -- probabilistic, selects most likely tokenization

## Related

- [[Vocabulary]] (token-to-ID mapping)
- [[Embeddings]] (tokens mapped to vectors)

---

#nlp #tokenization
