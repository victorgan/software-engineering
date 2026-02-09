# Runtime Impact

> <- Back to [[Cold Starts]]

Different runtimes have very different cold start characteristics. Interpreted languages (Python, Node.js) start fast (100-300ms). Compiled languages (Go, Rust) also start fast. JVM-based languages (Java, Scala) have the worst cold starts (1-10s) due to JVM warmup. GraalVM native images and SnapStart mitigate Java cold starts.

#cloud #serverless #performance
