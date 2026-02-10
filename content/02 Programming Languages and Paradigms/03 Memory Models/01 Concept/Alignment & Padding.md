# Alignment & Padding

> <- Back to [[Memory Layout]]

Compilers insert padding bytes between struct fields to satisfy hardware alignment requirements. Properly aligned data can be accessed in a single memory operation, while misaligned access may be slower or cause faults on some architectures. Cache line alignment is critical for performance.

## Key Properties

- [[Struct Layout]]
- [[Cache Line Alignment]]

---

#memory-models #memory-layout #alignment
