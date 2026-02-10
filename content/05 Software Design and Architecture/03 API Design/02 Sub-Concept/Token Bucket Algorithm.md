# Token Bucket Algorithm

> <- Back to [[Rate Limiting]]

A bucket holds a fixed number of tokens, replenished at a constant rate. Each request consumes a token. If the bucket is empty, the request is rejected. Allows bursts up to the bucket size while maintaining an average rate limit.

#property #rate-limiting #token-bucket
