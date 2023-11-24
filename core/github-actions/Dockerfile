FROM ubuntu:22.04

# Set environment variables
ENV DEBIAN_FRONTEND=noninteractive

# Update and install essential tools
RUN apt update && \
    apt install -y \
    build-essential \
    curl \
    wget \
    git \
    cmake \
    clang \
    gdb \
    && rm -rf /var/lib/apt/lists/*

# Install Rust
RUN curl https://sh.rustup.rs -sSf | sh -s -- -y

# Add Rust binaries to PATH
ENV PATH="/root/.cargo/bin:${PATH}"

# Display installed versions
RUN rustc --version && \
    cargo --version && \
    clang --version && \
    cmake --version && \
    gdb --version

# Set the default working directory
WORKDIR /workspace

# Set entry point to /bin/bash
CMD ["/bin/bash"]
