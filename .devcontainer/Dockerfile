FROM fedora:latest 

RUN useradd -ms /bin/bash vscode
USER root
RUN dnf install -y git golang
RUN dnf install dnf5-plugins && dnf config-manager addrepo --from-repofile=https://cli.github.com/packages/rpm/gh-cli.repo && dnf install -y gh --repo gh-cli

USER vscode
RUN mkdir -p /home/vscode/go