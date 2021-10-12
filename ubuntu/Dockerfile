FROM ubuntu:20.04
LABEL maintainer "Jamil André RAICHOUNI <raichouni@gmail.com>"
ENV SHELL = "/bin/bash"  # needed by poetry shell
ENV TZ="Europe/Berlin"
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime
RUN echo $TZ > /etc/timezone && \
    apt-get update --yes && \
    apt-get install --yes software-properties-common && \
    apt-get install --yes git && \
    apt-get install --yes vim && \
    apt autoremove --yes && \
    apt-get clean
CMD ["/bin/bash"]
