# python
FROM ubuntu:14.04
ENV DEBIAN_FRONTEND=noninteractive

RUN sudo apt-get install -y aptitude

RUN sudo DEBIAN_FRONTEND=noninteractive aptitude install -y software-properties-common
RUN sudo add-apt-repository ppa:fkrull/deadsnakes && sudo apt-get update
RUN sudo DEBIAN_FRONTEND=noninteractive aptitude install -y build-essential \
    curl \
    curl-dev \
    libcurl4-openssl-dev \
    libgeos-dev \
    libmemcached-dev \
    libncurses5-dev \
    libxml2-dev \
    libxslt1-dev \
    git
RUN sudo DEBIAN_FRONTEND=noninteractive aptitude build-dep -y libgeos-dev
RUN sudo DEBIAN_FRONTEND=noninteractive aptitude install -y python2.7 \
    python-dev

RUN curl https://bootstrap.pypa.io/get-pip.py | sudo python
RUN pip install virtualenv
RUN sudo easy_install lxml

RUN virtualenv --system-site-packages /src
RUN mkdir -p /src/logs
# RUN /bin/bash -c "source /src/bin/activate" && pip install -r docs/requirements.txt
