FROM ubuntu:14.04

RUN apt-get update -y && \
    apt-get upgrade -y && \
    apt-get install -y \
    build-essential \
    cmake \
    libboost-dev \
    libboost-filesystem-dev \
    libboost-system-dev \
    libboost-regex-dev \
    libboost-thread-dev \
    libprotoc-dev \
    libprotobuf-dev \
    protobuf-compiler \
    git-core \
    libswscale-dev \
    libgtk2.0-d \
    libavcodec-dev \
    libavformat-dev \
    libgflags-dev \
    yasm \
    libjsoncpp-dev \
    libboost-program-options-dev \
    libgoogle-glog-dev

RUN apt-get install -y \
    wget \
    unzip

RUN wget http://downloads.sourceforge.net/project/opencvlibrary/opencv-unix/2.4.9/opencv-2.4.9.zip && \
    unzip opencv-2.4.9.zip && \
    cd opencv-2.4.9 && \
    mkdir release && \
    cd release && \
    cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local .. && \
    sudo make && sudo make install && cd

RUN wget http://www.ffmpeg.org/releases/ffmpeg-2.2.3.tar.gz && \
    tar -zxvf ffmpeg-2.2.3.tar.gz && \
    cd ffmpeg-2.2.3 && \
    ./configure --enable-gpl && \
    sudo make && sudo make install && cd


