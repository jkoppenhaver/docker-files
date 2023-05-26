FROM ubuntu:22.04

RUN useradd -m administrator
#RUN echo 'administrator:password' | chpasswd
RUN usermod -aG sudo administrator
RUN passwd -d administrator
RUN apt-get update && apt-get upgrade -y && apt-get install -y sudo

USER administrator
WORKDIR /home/administrator
ENTRYPOINT bash
