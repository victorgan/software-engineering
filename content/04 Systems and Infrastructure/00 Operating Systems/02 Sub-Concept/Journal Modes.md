# Journal Modes

> <- Back to [[Journaling]]

Different levels of journaling protection. Journal mode journals both metadata and data (safest, slowest). Ordered mode journals metadata but writes data before metadata (default for ext4, good balance). Writeback mode journals only metadata (fastest, risk of stale data after crash).

#operating-systems #file-systems #reliability
