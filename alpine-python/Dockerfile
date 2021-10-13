FROM python:3.9.7-alpine3.14
LABEL maintainer "Jamil André RAICHOUNI <raichouni@gmail.com>"
ENV TZ="Europe/Berlin"
RUN pip install --upgrade pip && \
    pip install --no-cache-dir anybadge poetry-dynamic-versioning toml && \
    apk add --no-cache \
    curl \
    g++ \
    gcc \
    git \
    libressl-dev \
    musl-dev \
    libffi-dev && \
    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y --profile=minimal && \
    source $HOME/.cargo/env && \
    pip install --no-cache-dir poetry && \
    apk del \
    curl \
    libressl-dev \
    musl-dev \
    libffi-dev
CMD ["/bin/sh"]
