# python
FROM ubuntu:16.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && apt install -y build-essential \
    curl \
    curl-dev \
    libffi-dev \
    libssl-dev \
    libxml2-dev \
    libxslt1-dev \
    git \
    python2.7 \
    python2.7-dev \
    python-pip \
    python-virtualenv

WORKDIR /work

CMD ["bash"]
CMD ["python -v"]



# RUN DEBIAN_FRONTEND=noninteractive apt install -y software-properties-common
# RUN add-apt-repository ppa:fkrull/deadsnakes && sudo apt update
# RUN DEBIAN_FRONTEND=noninteractive apt install -y build-essential \
#     curl \
#     curl-dev \
#     libcurl4-openssl-dev \
#     libgeos-dev \
#     libmemcached-dev \
#     libncurses5-dev \
#     libxml2-dev \
#     libxslt1-dev \
#     git
# RUN DEBIAN_FRONTEND=noninteractive apt build-dep -y libgeos-dev
# RUN DEBIAN_FRONTEND=noninteractive apt install -y python2.7 \
#     python-dev
# 
# RUN curl https://bootstrap.pypa.io/get-pip.py | python
# RUN pip install virtualenv
# RUN easy_install lxml
# 
# RUN virtualenv --system-site-packages /src
# RUN mkdir -p /src/logs
# RUN /bin/bash -c "source /src/bin/activate" && pip install -r docs/requirements.txt
