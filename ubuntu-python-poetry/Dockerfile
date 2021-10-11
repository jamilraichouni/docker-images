FROM ubuntu:20.04
LABEL maintainer "Jamil André RAICHOUNI <raichouni@gmail.com>"
ENV TZ="Europe/Berlin"
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime
RUN echo $TZ > /etc/timezone && \
    apt-get update --yes && \
    apt-get install --yes software-properties-common && \
    apt-get install --yes git && \
    apt-get update && \
    add-apt-repository --yes ppa:deadsnakes/ppa && \
    apt-get update --yes && \
    apt-get install --yes python3.9 python3.9-venv && \
    apt-get remove --purge --yes python3.8 && \
    apt autoremove --yes && \
    ln -s /usr/bin/python3.9 /usr/local/bin/python && \
    ln -s /usr/bin/python3.9 /usr/local/bin/python3 && \
    ln -s /usr/bin/python3.9 /usr/local/bin/python3.9 && \
    update-alternatives --install /usr/bin/python python /usr/bin/python3.9 1 && \
    apt-get install --yes python3-pip && \
    apt-get clean && \
    pip install --no-cache-dir poetry poetry-dynamic-versioning
CMD ["/bin/bash"]
