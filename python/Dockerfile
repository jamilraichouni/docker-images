FROM registry.gitlab.com/jar1/docker-images/ubuntu:latest
LABEL maintainer "Jamil André RAICHOUNI <raichouni@gmail.com>"
ENV TZ="Europe/Berlin"

RUN apt-get purge --auto-remove python3* --yes && \
    ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && \
    echo $TZ > /etc/timezone && \
    apt-get install --yes software-properties-common && \
    apt-get update --yes && \
    add-apt-repository --yes ppa:deadsnakes/ppa && \
    apt-get update --yes && \
    apt-get install --yes python3.9 python3.9-venv && \
    apt autoremove --yes && \
    apt-get install --yes --no-install-recommends python3-pip && \
    apt-get clean && \
    ln -s /usr/bin/python3.9 /usr/local/bin/python3 && \
    update-alternatives --install /usr/local/bin/python3 python3 /usr/bin/python3.9 1 && \
    export PATH=/usr/local/bin:$PATH && \
    rm /usr/bin/python3 && \
    rm /usr/bin/pip* && \
    ln -s /usr/bin/python3.9 /usr/bin/python3 && \
    python3 -m pip install --no-cache-dir cookiecutter poetry poetry-dynamic-versioning

CMD ["/bin/bash"]
