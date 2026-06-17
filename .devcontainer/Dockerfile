FROM mcr.microsoft.com/devcontainers/base:ubuntu-24.04
RUN curl -fsSL https://mise.jdx.dev/install.sh | MISE_INSTALL_PATH=/usr/local/bin/mise bash
ENV PATH="/home/vscode/.local/share/mise/shims:/usr/local/bin:$PATH"
RUN echo 'eval "$(mise activate bash)"' >> /home/vscode/.bashrc && \
    echo 'eval "$(mise activate zsh)"' >> /home/vscode/.zshrc
