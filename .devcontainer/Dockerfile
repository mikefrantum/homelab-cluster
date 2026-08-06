FROM mcr.microsoft.com/devcontainers/base:ubuntu-24.04
RUN curl -fsSL https://mise.jdx.dev/install.sh | MISE_INSTALL_PATH=/usr/local/bin/mise bash
ENV PATH="/home/vscode/.local/share/mise/shims:/usr/local/bin:$PATH"
RUN apt-get update && apt-get install -y keychain && rm -rf /var/lib/apt/lists/*
RUN echo 'eval "$(mise activate bash)"' >> /home/vscode/.bashrc && \
    echo 'eval "$(mise activate zsh)"' >> /home/vscode/.zshrc && \
    echo 'eval $(keychain --eval --quiet id_ed25519)' >> /home/vscode/.bashrc && \
    echo 'eval $(keychain --eval --quiet id_ed25519)' >> /home/vscode/.zshrc
RUN sh -c "$(curl -fsLS get.chezmoi.io)" -- -b /usr/local/bin

