# Claude Code self-hosted runner image for Pegasus WMS development.
# https://code.claude.com/docs/en/self-hosted-environments-deploy

FROM rockylinux/rockylinux:10

# Claude binary
RUN <<EOT
curl -fsSL https://claude.ai/install.sh | bash
mv ~/.local/bin/claude /usr/local/bin/claude
EOT

ENTRYPOINT ["claude"]
