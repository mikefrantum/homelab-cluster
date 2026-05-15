
● The >> creates it if it doesn't exist. But to be safe, create it properly with bash profile structure:

  FROM mcr.microsoft.com/devcontainers/base:ubuntu-24.04

  COPY --from=jdxcode/mise /usr/local/bin/mise /usr/local/bin/

  RUN echo '[ -f ~/.bashrc ] && source ~/.bashrc' >> /home/vscode/.bash_profile && \
      echo 'eval "$(mise activate bash)"' >> /home/vscode/.bash_profile && \
      echo 'eval "$(mise activate zsh)"' >> /home/vscode/.zshrc
