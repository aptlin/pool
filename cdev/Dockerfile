FROM ubuntu:xenial
LABEL maintainer="Sasha Illarionov <sasha.delly@gmail.com>"
ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update -qq && apt-get install -y --no-install-recommends \
    git \
    curl \
    wget \
    python \
    python3 \
    build-essential \
    ca-certificates \
    cmake \
    clang \
    gdb \
    valgrind \
    bsdmainutils

# set up cpplint
RUN apt-get install -y python3-pip

RUN pip3 install --upgrade pip
RUN pip3 install cpplint
RUN rm -rf /tmp/* /var/lib/apt/lists/*

ENV \
    CC="/usr/bin/clang" \
    CXX="/usr/bin/clang++"

COPY bin/mk /usr/bin/
RUN chmod +x /usr/bin/mk
COPY bin/c+ /usr/bin/
RUN chmod +x /usr/bin/c+

WORKDIR /data
VOLUME ["/data"]