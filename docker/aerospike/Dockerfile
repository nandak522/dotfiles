# aerospike
FROM ubuntu:14.04
ENV DEBIAN_FRONTEND=noninteractive
ENV AEROSPIKE_VERSION 3.7.5.1

RUN sudo apt-get update && sudo apt-get install -y aptitude
RUN sudo DEBIAN_FRONTEND=noninteractive aptitude install -y build-essential

RUN sudo DEBIAN_FRONTEND=noninteractive aptitude install -y curl
RUN curl -L http://aerospike.com/download/server/latest/artifact/ubuntu14 | tar xvz
RUN cd /aerospike-server-community-${AEROSPIKE_VERSION}-ubuntu14.04 && sudo DEBIAN_FRONTEND=noninteractive ./asinstall
RUN sudo DEBIAN_FRONTEND=noninteractive  /etc/init.d/aerospike start
# Expose Aerospike ports
#
#   3000 – service port, for client connections
#   3001 – fabric port, for cluster communication
#   3002 – mesh port, for cluster heartbeat
#   3003 – info port
#
EXPOSE 3000 3001 3002 3003
ENTRYPOINT ["asd"]
CMD ["--foreground"]
