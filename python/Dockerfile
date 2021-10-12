FROM registry.gitlab.com/jar1/docker-images/ubuntu:latest
LABEL maintainer "Jamil André RAICHOUNI <raichouni@gmail.com>"
ENV TZ="Europe/Berlin"

RUN apt-get purge --auto-remove python3* --yes

RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime
RUN echo $TZ > /etc/timezone
RUN apt-get install --yes software-properties-common

RUN apt-get update --yes
RUN add-apt-repository --yes ppa:deadsnakes/ppa
RUN apt-get update --yes

RUN apt-get install --yes python3.9 python3.9-venv
RUN apt autoremove --yes
RUN apt-get install --yes --no-install-recommends python3-pip
RUN apt-get clean
RUN ln -s /usr/bin/python3.9 /usr/local/bin/python3
RUN update-alternatives --install /usr/local/bin/python3 python3 /usr/bin/python3.9 1
RUN export PATH=/usr/local/bin:$PATH
RUN rm /usr/bin/python3
RUN rm /usr/bin/pip*
RUN ln -s /usr/bin/python3.9 /usr/bin/python3
RUN python3 -m pip install --no-cache-dir cookiecutter poetry poetry-dynamic-versioning
CMD ["/bin/bash"]
