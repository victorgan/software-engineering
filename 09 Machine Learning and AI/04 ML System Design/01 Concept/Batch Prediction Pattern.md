# Batch Prediction Pattern

> <- Back to [[ML System Design Patterns]]

Pre-compute predictions offline, serve from cache/DB. Low latency at serving time but stale predictions. Good for recommendation emails, daily reports, and non-time-sensitive predictions.

## Related

- [[Real-Time Prediction Pattern]] (fresh but slower)
- [[Batch Inference]] (implementation)

---

#ml-system-design #batch-prediction
