# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.ssh.forward_agent = true
  config.ssh.forward_x11 = true
  config.vm.box = "ubuntu/xenial64"
  config.vm.synced_folder "epigrass-data/", "/home/ubuntu", create: true
  config.vm.provision "shell", inline: <<-SHELL
    export CPLUS_INCLUDE_PATH=/usr/include/gdal
    export C_INCLUDE_PATH=/usr/include/gdal
    apt-get update
    sudo apt-get install \
      build-essential \
      libgdal-dev \
      libqt4-opengl \
      python \
      python-dev \
      python-matplotlib \
      python-matplotlib-data \
      python-matplotlib-doc \
      python-mysqldb \
      python-numpy \
      python-pip \
      python-qt4-gl \
      python-qwt5-qt4 \
      python-setuptools \
      redis-server \
      xauth \
      --yes
    pip install --upgrade pip
    pip install GDAL==1.10.0 Cython pymysql
    pip install epigrass 
  SHELL

end
