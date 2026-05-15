FROM mcr.microsoft.com/devcontainers/base:ubuntu-24.04

  COPY --from=jdxcode/mise /usr/local/bin/mise /usr/local/bin/

  ENV PATH="/home/vscode/.local/share/mise/shims:$PATH"

  RUN echo 'eval "$(mise activate bash)"' >> /home/vscode/.bashrc && \
      echo 'eval "$(mise activate zsh)"' >> /home/vscode/.zshrc
