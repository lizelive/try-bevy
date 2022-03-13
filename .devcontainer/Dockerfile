# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.224.2/containers/rust/.devcontainer/base.Dockerfile

# [Choice] Debian OS version (use bullseye on local arm64/Apple Silicon): buster, bullseye
ARG VARIANT="bullseye"
FROM mcr.microsoft.com/vscode/devcontainers/rust:0-${VARIANT}
#FROM lscr.io/linuxserver/webtop:${VARIANT}
# FROM nvidia/opengl:1.2-glvnd-devel

# [Optional] Uncomment this section to install additional packages.
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends x11-apps libasound2-dev libxrandr2 libxi-dev libx11-xcb1 freeglut3-dev \
    libxau6 libxdmcp6 libxcb1 libxext6 libx11-6 \
    libglvnd0 libgl1 libglx0 libegl1 libgles2 \
    libglvnd-dev libgl1-mesa-dev libegl1-mesa-dev libgles2-mesa-dev \
    libglx-dev libgl1-mesa-glx libgl1-mesa-dri mesa-utils

# ENV NVIDIA_VISIBLE_DEVICES \
#         ${NVIDIA_VISIBLE_DEVICES:-all}
# ENV NVIDIA_DRIVER_CAPABILITIES \
#         ${NVIDIA_DRIVER_CAPABILITIES:+$NVIDIA_DRIVER_CAPABILITIES,}graphics,compat32,utility

# RUN  echo "/usr/local/nvidia/lib" >> /etc/ld.so.conf.d/nvidia.conf && echo "/usr/local/nvidia/lib64" >> /etc/ld.so.conf.d/nvidia.conf
    
# ENV LD_LIBRARY_PATH /usr/lib/x86_64-linux-gnu:/usr/lib/i386-linux-gnu${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}:/usr/local/nvidia/lib:/usr/local/nvidia/lib64