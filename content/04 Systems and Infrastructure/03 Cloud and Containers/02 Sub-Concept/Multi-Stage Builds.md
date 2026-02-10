# Multi-Stage Builds

> <- Back to [[Docker]]

Using multiple FROM statements in a Dockerfile to separate build and runtime stages. The build stage includes compilers and build tools; the final stage copies only the compiled artifacts into a minimal base image. Dramatically reduces image size (e.g., Go binary: 1GB build image to 10MB runtime image).

#cloud #containers #docker
