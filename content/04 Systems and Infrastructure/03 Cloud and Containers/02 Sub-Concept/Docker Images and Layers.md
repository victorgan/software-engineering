# Docker Images and Layers

> <- Back to [[Docker]]

Images are built as a stack of read-only layers, each representing a Dockerfile instruction. Layers are cached and shared between images, saving storage and build time. The container adds a thin writable layer on top. Changing an early layer invalidates all subsequent cached layers — order Dockerfile instructions accordingly.

#cloud #containers #docker
