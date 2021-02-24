FROM nvcr.io/nvidia/caffe:20.03-py3

RUN apt-get update
RUN apt-get install -y liblapack-dev python-numpy python-pip

RUN python2 -m pip install scikit-image protobuf

#Dealing with cmake. Replacing for newer version
RUN apt-get remove --purge cmake -y

WORKDIR /tmp
RUN wget https://cmake.org/files/v3.19/cmake-3.19.1-Linux-x86_64.sh 
RUN mkdir /opt/cmake
RUN sh cmake-3.19.1-Linux-x86_64.sh --skip-license --prefix=/opt/cmake
RUN ln -s /opt/cmake/bin/cmake /usr/local/bin/cmake

WORKDIR /home


