# Copyright (c) 2023 RFull Development
# This source code is managed under the MIT license. See LICENSE in the project root.
ARG NODE_VERSION
ARG INSTALL_PACKAGES

FROM node:${NODE_VERSION}

# Setup
RUN apt update && \
    apt install -y sudo ${INSTALL_PACKAGES}
RUN echo "node ALL=(ALL:ALL) NOPASSWD:ALL" > /etc/sudoers.d/node

# Clean up
RUN sudo apt clean && \
    sudo rm -rf /var/lib/apt/lists/*

USER node
