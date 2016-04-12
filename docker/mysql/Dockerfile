# database
FROM ubuntu:14.04
ENV DEBIAN_FRONTEND=noninteractive
RUN sudo apt-get update && sudo apt-get install -y aptitude
RUN sudo aptitude install -y build-essential \
    libmysqlclient-dev
RUN sudo DEBIAN_FRONTEND=noninteractive MYSQL_ROOT_PASSWORD=root aptitude install -f -y \
    mysql-server-5.6 \
    mysql-client-5.6 \
    mysql-client-core-5.6
