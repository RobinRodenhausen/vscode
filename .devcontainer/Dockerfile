FROM ubuntu:rolling

# Install OS packages
RUN apt-get update \
    && apt-get dist-upgrade -y \
    && apt-get install -y curl git jq nano sudo unzip vim wget zip \
    && apt-get clean

# TODO: Add relevant software here

RUN echo 'ubuntu ALL=(ALL:ALL) NOPASSWD: ALL' > /etc/sudoers.d/ubuntu \
    && chmod 0440 /etc/sudoers.d/ubuntu

USER ubuntu
WORKDIR /home/ubuntu

# Shell
RUN curl --silent https://raw.githubusercontent.com/RobinRodenhausen/shell/main/setup.sh | bash

CMD [ "sleep", "infinity" ]
