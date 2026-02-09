# Snapshot Support

> <- Back to [[Copy-on-Write]]

Copy-on-write enables instant, space-efficient snapshots by simply preserving the current metadata pointers. New writes go to new locations while the snapshot continues to reference the original blocks. ZFS and Btrfs leverage this for backup, rollback, and data protection.

#operating-systems #file-systems
