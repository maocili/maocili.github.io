+++
title = 'dockerfile'
description = 'dockerfile 打包'
date = '2020-06-17'
tags = ['dcoker', 'dockerfile']
showToc = true
+++

``` dockerfile
#定义来源镜像
FROM centos:7  
ENV container docker

# 在镜像中运行命令
RUN yum -y install wget
RUN yum -y install setup 

#配置环境变量（这里只能使用ENV配置，直接修改/etc/profile 文件无法生效）
ENV PATH $PATH:/go/bin:/node-v12/bin

#复制文件到镜像中
COPY ./gopl-zh.github.com-master/* /gopl-zh/

#设置工作目录，RUN执行时所在的目录
WORKDIR /gopl-zh

#暴露端口
EXPOSE 4000

docker build -t="test" .
