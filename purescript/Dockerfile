FROM ubuntu:latest

RUN apt-get update
RUN apt-get install -y curl git vim

RUN curl -sL https://deb.nodesource.com/setup_8.x | bash -
RUN apt-get install -y nodejs


RUN curl -L -O https://github.com/purescript/purescript/releases/download/v0.11.7/linux64.tar.gz
RUN gzip -dcv ./linux64.tar.gz | tar -xvf -
RUN mv ./purescript/p* /usr/local/bin
RUN rm -rf ./purescript
RUN rm ./linux64.tar.gz

RUN npm install -g pulp bower

RUN adduser purescript

USER purescript
