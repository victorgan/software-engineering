# Crash Recovery

> <- Back to [[Journaling]]

On reboot after a crash, the file system checks the journal for incomplete transactions. Complete transactions in the journal are replayed; incomplete ones are discarded. This recovery is much faster than a full file system check (fsck) on non-journaling systems.

#operating-systems #file-systems #reliability
