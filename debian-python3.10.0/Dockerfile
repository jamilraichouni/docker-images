FROM python:3.10.0-slim-buster
LABEL maintainer "Jamil André RAICHOUNI <raichouni@gmail.com>"
LABEL org.opencontainers.image.source https://github.com/jamilraichouni/docker-images
ENV TZ="Europe/Berlin"
RUN pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir anybadge poetry poetry-dynamic-versioning toml && \
    apt-get update && \
    apt-get install --yes \
    git \
    vim && \
    git config --global init.defaultBranch main && \
    apt autoremove --yes && \
    apt-get clean && \
    find /usr/local/lib/python3.10 -depth -type d -name '__pycache__' -exec rm -Rf {} \; && \
    find /usr/local/lib/python3.10 -depth -type f -name '*.pyc' -exec rm -f {} \; && \
    rm -rf /var/lib/apt/lists/ && \
    echo "alias l='ls -l'" >> ~/.bashrc && \
    echo "alias ll='ls -lah'" >> ~/.bashrc && \
    # source changes:
    . ~/.bashrc

CMD ["/bin/bash"]
