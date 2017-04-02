FROM ubuntu:16.04
LABEL maintainer "Nanda Kishore <madhav.bnk@gmail.com>"
RUN apt-get update && apt-get install -y automake \
	build-essential \
	curl \
	python-dev \
    && rm -rf /var/lib/apt/lists/*
RUN curl https://bootstrap.pypa.io/get-pip.py | python
RUN pip install virtualenv
ENTRYPOINT ["python"]
CMD ["--version"]
