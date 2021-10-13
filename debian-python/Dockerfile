FROM python:3.9.7-slim-buster
LABEL maintainer "Jamil André RAICHOUNI <raichouni@gmail.com>"
ENV TZ="Europe/Berlin"
RUN pip install --upgrade pip && \
    pip install --no-cache-dir anybadge poetry-dynamic-versioning && \
    pip install --no-cache-dir poetry && \
    apt-get update && \
    apt-get install --yes git && \
    apt autoremove --yes && \
    apt-get clean
CMD ["/bin/sh"]
