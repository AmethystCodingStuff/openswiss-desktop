# Use stable bookworm base
FROM mcr.microsoft.com/vscode/devcontainers/base:bookworm

# Install extra dev tools
RUN apt-get update && \
    apt-get install -y git curl build-essential python3 python3-pip && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

# Set default shell for vscode user
SHELL ["/bin/bash", "-c"]

# Switch to non-root user
USER vscode

# Set workdir
WORKDIR /workspace
