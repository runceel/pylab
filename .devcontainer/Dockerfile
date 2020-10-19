# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.145.0/containers/ubuntu/.devcontainer/base.Dockerfile

# [Choice] Ubuntu version: bionic, focal
# ARG VARIANT="bionic"
# FROM mcr.microsoft.com/vscode/devcontainers/base:0-${VARIANT}
FROM ubuntu

RUN apt-get update && apt-get -y upgrade && \
    apt-get install libgl1-mesa-glx libegl1-mesa libxrandr2 libxrandr2 libxss1 libxcursor1 libxcomposite1 libasound2 libxi6 libxtst6 git wget -y && \
    wget -P /opt https://repo.anaconda.com/archive/Anaconda3-2020.07-Linux-x86_64.sh && \
    bash /opt/Anaconda3-2020.07-Linux-x86_64.sh -b -p /opt/anaconda3 && \
    rm /opt/Anaconda3-2020.07-Linux-x86_64.sh
RUN echo "export PATH=/opt/anaconda3/bin:$PATH" >> ~/.bashrc && \
    cat ~/.bashrc && \
    . ~/.bashrc && \
    conda init
