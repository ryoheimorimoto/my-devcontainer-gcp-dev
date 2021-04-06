# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.166.0/containers/debian/.devcontainer/base.Dockerfile

# [Choice] Debian version: buster, stretch
FROM google/cloud-sdk:latest

# ** [Optional] Uncomment this section to install additional packages. **
RUN apt update -y && export DEBIAN_FRONTEND=noninteractive

# for Go
RUN apt -y install software-properties-common
RUN add-apt-repository -y ppa:longsleep/golang-backports
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys F6BC817356A3D45E
RUN apt update -y && apt install -y golang

# for Node.js / TypeScript
RUN apt -y install nodejs npm
RUN npm install -g typescript ts-node

# Utility
RUN echo "alias ll='ls -al'" >> /root/.bashrc
RUN echo "alias g='gcloud'" >> /root/.bashrc
