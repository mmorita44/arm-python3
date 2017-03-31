FROM hypriot/rpi-alpine-scratch:edge
MAINTAINER Masato Morita <m.morita44@hotmail.com>

ENV PYTHON_VERSION 3.6.1-r0
ENV PYTHON_PIP_VERSION 9.0.1

# install python3
RUN apk add --no-cache curl python3=$PYTHON_VERSION python3-dev=$PYTHON_VERSION && \
# install pip3
    curl -Ls https://bootstrap.pypa.io/get-pip.py -o /tmp/get-pip.py && \
    python3 /tmp/get-pip.py pip==$PYTHON_PIP_VERSION && \
    rm /tmp/get-pip.py && \
    apk del curl

CMD ["python3"]
