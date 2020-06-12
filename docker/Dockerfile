FROM debian:buster

RUN apt-get update \
 && apt-get install --no-install-recommends -y build-essential \
    gcc \
    unzip \
    wget \
    zip \
    gcc-avr \
    binutils-avr \
    avr-libc \
    dfu-programmer \
    dfu-util \
    gcc-arm-none-eabi \
    binutils-arm-none-eabi \
    libnewlib-arm-none-eabi \
    python3 \
    python3-pip \
    python3-setuptools \
    git \
 && apt-get clean

RUN python3 --version && python3 -m pip install qmk

ENV keyboard=crkbd
ENV keymap=default

VOLUME /qmk
WORKDIR /qmk
