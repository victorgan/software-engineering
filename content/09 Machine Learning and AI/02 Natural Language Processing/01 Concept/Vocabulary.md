# Vocabulary

> <- Back to [[Text Processing Pipeline]]

The mapping from tokens to integer IDs that the model uses. Includes special tokens for specific model needs.

## Key Properties

- Token-to-ID mapping (lookup table)
- Special tokens: [CLS] (classification), [SEP] (separator), [PAD] (padding), [MASK] (masking), [BOS]/[EOS] (begin/end of sequence)
- Vocabulary size tradeoff: larger = better coverage but more parameters

## Related

- [[Tokenization]] (determines the vocabulary)
- [[Embeddings]] (each vocab entry gets an embedding vector)

---

#nlp #vocabulary
