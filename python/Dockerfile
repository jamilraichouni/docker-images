FROM python:3.9.7
COPY . /tmp/mytest
WORKDIR /tmp/mytest
RUN pip install --no-cache-dir poetry poetry-dynamic-versioning && \
    poetry install
CMD ["/bin/bash"]
ENTRYPOINT ["/bin/bash"]
