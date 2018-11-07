FROM ubuntu:16.04
RUN sed -i 's/archive.ubuntu.com/mirrors.ustc.edu.cn/g' /etc/apt/sources.list
RUN sed -i 's/security.ubuntu.com/mirrors.ustc.edu.cn/g' /etc/apt/sources.list

RUN mkdir /data
WORKDIR /data
# RUN apt-get update \
#     && apt-get install -y supervisor \
#     && rm -rf /var/lib/apt/lists/*
ADD discovery /data
