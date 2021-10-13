FROM python:3.9.7-alpine
LABEL maintainer "Jamil André RAICHOUNI <raichouni@gmail.com>"
ENV TZ="Europe/Berlin"
RUN /usr/local/bin/python3 -m pip install --upgrade pip && \
    python3 -m pip install --no-cache-dir --only-binary ":all:" anybadge poetry poetry-dynamic-versioning
CMD ["/bin/sh"]
