# VoltDB on top of Docker base JDK8 images
FROM java:8
MAINTAINER Theodore Omtzigt <theo@stillwater-sc.com>

RUN apt-get update && apt-get install bash wget && \
    mkdir -p /root/voltdb && cd /root/voltdb && \
    wget http://downloads.voltdb.com/technologies/server/voltdb-ent-latest.tar.gz && \
    tar -xzf voltdb-ent-latest.tar.gz && \
    cd voltdb-ent-*

CMD ["bin/voltdb create"]
