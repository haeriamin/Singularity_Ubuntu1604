Bootstrap: docker
From: ubuntu:16.04

%labels
  Author Amin Haeri
  
%post
  apt-get update --fix-missing
  apt-get install -yq \
    cmake \
    curl \
    g++ \
    git \
    graphviz-dev \
    libcfitsio-dev \
    libfftw3-dev \
    libftgl-dev \
    libglew-dev \
    libglu1-mesa-dev \
    libgsl-dev \
    libjpeg-dev \
    libkrb5-dev \
    libldap2-dev \
    libmysqlclient-dev \
    libpcre3-dev \
    libpng-dev \
    libqt4-dev \
    libqt4-opengl-dev \
    libssl-dev \
    libtbb-dev \
    libx11-dev \
    libxext-dev \
    libxft-dev \
    libxi-dev \
    libxml2-dev \
    libxmu-dev \
    libxpm-dev \
    libxt-dev \
    make \
    python-dev \
    rsync \
    tcl \
    wget
    
  apt-get install -y python3-dev git build-essential cmake make g++ libx11-dev

  mkdir -p /opt
  curl -sL https://root.cern.ch/download/root_v6.14.00.Linux-ubuntu16-x86_64-gcc5.4.tar.gz | tar -C /opt -zxf -

  apt-get clean
  apt-get autoclean
  rm -rf /var/lib/apt/lists/*

%environment
  export ROOTSYS=/opt/root
  export PATH=$ROOTSYS/bin:$PATH
  export PYTHONPATH=$ROOTSYS/lib:$PYTHONPATH
  export LD_LIBRARY_PATH=$ROOTSYS/lib:$LD_LIBRARY_PATH
