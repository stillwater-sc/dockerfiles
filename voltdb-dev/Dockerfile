# VoltDB on top of Docker base JDK8 images
FROM java:8
MAINTAINER Theodore Omtzigt <theo@stillwater-sc.com>

RUN apt-get update && apt-get install bash wget \
    ant build-essential ant-optional default-jdk python cmake \
    valgrind ntp ccache git-arch git-completion git-core git-svn git-doc \
    git-email python-httplib2 python-setuptools python-dev apt-show-versions && \
    mkdir -p /root/voltdb && cd /root/voltdb && \
    git clone https://github.com/VoltDB/voltdb.git && cd voltdb \
    ant clean
    
WORKDIR /root/voltdb/voltdb
CMD ["bash"]
