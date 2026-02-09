# Data Integrity Verification

> <- Back to [[Copy-on-Write]]

CoW file systems like ZFS store checksums for every data block and verify them on read, detecting silent data corruption (bit rot). The tree structure of checksums means corruption anywhere in the data path is detectable, unlike traditional file systems.

#operating-systems #file-systems #reliability
