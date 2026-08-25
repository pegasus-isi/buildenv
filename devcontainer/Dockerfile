# Pegasus devcontainer image for Ubuntu 24.04.

FROM mcr.microsoft.com/devcontainers/base:ubuntu-24.04

RUN <<EOT
set -evx
export DEBIAN_FRONTEND=noninteractive

apt-get -y update
apt-get -y install --no-install-recommends ca-certificates curl gnupg

# HTCondor
mkdir -p /etc/apt/keyrings
curl -fsSL https://htcss-downloads.chtc.wisc.edu/repo/keys/HTCondor-25.x-Key -o /etc/apt/keyrings/htcondor.asc
curl -fsSL https://htcss-downloads.chtc.wisc.edu/repo/ubuntu/htcondor-25.x-noble.list -o /etc/apt/sources.list.d/htcondor.list
apt-get -y update
apt-get -y install minicondor
sed -i 's/condor@/vscode@/g' /etc/condor/config.d/00-minicondor

# git + basic CLI tools (git config/clone/push, tar/unzip for release-tools scripts).
apt-get -y install --no-install-recommends \
    git openssh-client \
    tar gzip unzip which jq

# Pegasus runtime dependencies
apt-get -y install --no-install-recommends \
    tar \
    curl wget \
    vim nano emacs \
    sudo \
    locales-all \
    graphviz

# Pegasus build dependencies
apt-get -y install --no-install-recommends \
    ant \
    ant-optional \
    bc \
    build-essential \
    cmake \
    createrepo-c \
    debhelper \
    debsigs \
    default-jdk \
    dpkg-dev \
    gnupg \
    graphviz \
    latexmk \
    lintian \
    libbz2-dev \
    libcurl4-openssl-dev \
    libffi-dev \
    libmysqlclient-dev \
    libpq-dev \
    libreadline-dev \
    libsqlite3-dev \
    libssl-dev \
    mpich \
    patch \
    pinentry-tty \
    python3-dev \
    python3-git \
    python3-openssl \
    python3-pip \
    python3-pytest \
    python3-setuptools \
    python3-setuptools-scm \
    python3-sphinx \
    python3-venv \
    python3-yaml \
    python3-build \
    python3-scikit-build-core \
    texlive-latex-extra \
    tox \
    zlib1g-dev \
    golang-go

# uv + dev tool venvs
curl -LsSf https://astral.sh/uv/install.sh | env UV_INSTALL_DIR=/usr/local/bin sh

su -s /bin/bash vscode <<EOS
uv tool install codespell
uv tool install commitizen
uv tool install gha-update
uv tool install mdformat --with mdformat-gfm
uv tool install mypy
uv tool install pre-commit
uv tool install pytest
uv tool install pyupgrade
uv tool install ruff
uv tool install sphinx
uv tool install tox --with tox-uv
uv tool install twine
EOS

cp -f /usr/share/zoneinfo/America/Los_Angeles /etc/localtime

chmod -R 775 /home/vscode
chown -R vscode:vscode /home/vscode

echo "vscode ALL=(root) NOPASSWD:ALL" > /etc/sudoers.d/vscode
chmod 0440 /etc/sudoers.d/vscode

# Cleanup
apt-get clean
rm -rf /var/lib/apt/lists/*
EOT

ENV LANG=en_US.UTF-8

USER vscode
CMD ["/bin/bash"]
