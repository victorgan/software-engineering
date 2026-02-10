# Lazy Loading

> <- Back to [[Memory-Mapped Files]]

Memory-mapped file contents are not loaded into RAM until accessed. The OS loads pages on demand via page faults, meaning only the portions of the file actually used consume physical memory. This is efficient for large files where only a subset is needed.

#operating-systems #memory #io
