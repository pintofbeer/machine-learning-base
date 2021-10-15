# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.202.3/containers/ubuntu/.devcontainer/base.Dockerfile

# [Choice] Ubuntu version (use hirsuite or bionic on local arm64/Apple Silicon): hirsute, focal, bionic
ARG VARIANT="hirsute"
FROM mcr.microsoft.com/vscode/devcontainers/base:0-${VARIANT}

# [Optional] Uncomment this section to install additional OS packages.
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends python3-dev python3-pip python3-venv

RUN su vscode -c "pip3 install --user --upgrade tensorflow ipykernel scikit-learn matplotlib" 2>&1