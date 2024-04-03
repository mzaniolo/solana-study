FROM mcr.microsoft.com/vscode/devcontainers/rust

RUN sh -c "$(curl -sSfL https://release.solana.com/stable/install)" && export PATH="/home/vscode/.local/share/solana/install/active_release/bin:$PATH"

RUN cargo install --git https://github.com/coral-xyz/anchor avm --locked --force && avm install latest && avm use latest

RUN sudo apt-get -y install libudev-dev && cargo install spl-token-cli
