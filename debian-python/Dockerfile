FROM python:3.9.7-slim-buster
LABEL maintainer "Jamil André RAICHOUNI <raichouni@gmail.com>"
ENV TZ="Europe/Berlin"
RUN pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir anybadge poetry poetry-dynamic-versioning toml && \
    apt-get update && \
    apt-get install --yes git && \
    apt autoremove --yes && \
    apt-get clean && \
    find /usr/local/lib/python3.9 -depth -type d -name '__pycache__' -exec rm -Rf {} \ && \
    find /usr/local/lib/python3.9 -depth -type f -name '*.pyc' -exec rm -f {} \ && \
    rm -rf /var/lib/apt/lists/
CMD ["/bin/sh"]
