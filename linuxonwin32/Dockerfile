FROM ubuntu:18.04
ENV DEBIAN_FRONTEND=noninteractive
#lang added for failure in ansible pip install
RUN apt-get update && apt-get install -y locales && rm -rf /var/lib/apt/lists/* \
 && locale-gen "en_US.UTF-8"
ENV LANG=en_US.UTF-8 \
    LANGUAGE=en_US:en \
    LC_ALL=en_US.UTF-8  
RUN apt-get update && apt-get install -y gcc git python-dev libkrb5-dev && \
  apt-get install python3-pip sudo git -y &&  \
  pip3 install --upgrade pip --proxy=http://UNISOURCE%5Cgisbatch:Sun556%23%23%@10.128.22.80:8080 && \
  pip3 install --upgrade virtualenv --proxy=http://UNISOURCE%5Cgisbatch:Sun556%23%23%@10.128.22.80:8080 && \
  pip3 install pywinrm[kerberos] --proxy=http://UNISOURCE%5Cgisbatch:Sun556%23%23%@10.128.22.80:8080 &&  \
  apt install krb5-user -y && \ 
  pip3 install pywinrm --proxy=http://UNISOURCE%5Cgisbatch:Sun556%23%23%@10.128.22.80:8080 && \
  pip3 install ansible --proxy=http://UNISOURCE%5Cgisbatch:Sun556%23%23%@10.128.22.80:8080
