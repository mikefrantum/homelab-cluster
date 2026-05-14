FROM mcr.microsoft.com/devcontainers/base:ubuntu-24.04

COPY --from=jdxcode/mise /usr/local/bin/mise /usr/local/bin/

# Create homelab user
RUN useradd -m -s /bin/bash homelab

# Activate mise for homelab
RUN echo 'eval "$(mise activate bash)"' >> /home/homelab/.bashrc && \
  echo 'eval "$(mise activate zsh)"' >> /home/homelab/.zshrc

