# Initialization Latency

> <- Back to [[Cold Starts]]

The time to create a new execution environment: provisioning a micro-VM or container, loading the runtime, downloading code, and running initialization code. Python/Node.js typically 100-500ms; Java/C# can be 1-10 seconds due to JVM/.NET startup. Minimized by keeping deployment packages small.

#cloud #serverless #performance
