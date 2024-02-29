FROM nvidia/cuda:11.8.0-runtime-ubuntu20.04
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get -qq update \
    && apt-get install -qqy --no-install-recommends \
    curl \
    python3-dev \
    gcc nano \
    ffmpeg libasound-dev portaudio19-dev libportaudio2 libportaudiocpp0 \
    postgresql postgresql-contrib -y && \
    rm -rf /var/lib/apt/lists/*
RUN curl https://bootstrap.pypa.io/get-pip.py | python3 -
RUN pip install poetry
WORKDIR /code
