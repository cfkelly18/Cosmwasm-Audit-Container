FROM rust:latest

WORKDIR /workspace

RUN apt-get update \
    && apt-get install -y build-essential make \
    && cargo install honggfuzz \
    && cargo install cargo-tarpaulin

RUN rustup component add clippy


# Feel free to adjust but its better than the vanilla shell
RUN apt-get update && apt-get install -y zsh
RUN sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" --unattended
SHELL ["zsh", "-c"]

# running as non-root user
RUN useradd -ms /bin/bash auditor
USER auditor

