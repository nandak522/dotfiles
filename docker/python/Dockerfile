FROM ubuntu:14.04
RUN sudo apt-get autoclean
RUN sudo apt-get clean
RUN sudo apt-get autoremove
RUN sudo apt-get install -y aptitude
RUN sudo aptitude install -y build-essential \
    curl \
    python-dev
RUN curl https://bootstrap.pypa.io/get-pip.py | sudo python
RUN pip install virtualenv
