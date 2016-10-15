FROM ubuntu:14.04

RUN apt-get update -y && \
    apt-get install -y \
    git \ 
    haskell-platform

RUN cabal update && \
    cabal install Cabal cabal-install

RUN git clone https://github.com/JacopoTeneggi/data-science-studies.git /hxlmath && cd /hxlmath && git checkout hxlmath