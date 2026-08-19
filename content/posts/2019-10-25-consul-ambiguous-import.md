+++
title = 'consul版本冲突报错'
description = '已解决'
date = '2019-10-25'
tags = ['golang', 'consul', '服务注册', '报错处理', 'go mod']
showToc = true
+++

## go version

go version go1.13

### build error info

> build command-line-arguments: cannot load github.com/hashicorp/consul/api: ambiguous import: found > github.com/hashicorp/consul/api in multiple modules:
>
> github.com/hashicorp/consul v1.4.2 (C:\Users\Administrator\go\pkg\mod\github.com\hashicorp\consul@v1.4.2\api)
>
> github.com/hashicorp/consul/api v1.0.1 (C:\Users\Administrator\go\pkg\mod\github.com\hashicorp\consul\api@v1.0.1)

### 原因

> 安装多个版本的 consul 导致引入处突

### 解决方案

> 可参考 https://github.com/hashicorp/consul/issues/6019
>
> 删除本地已存在的 consul 现有版本，**_清除 go.mod 文件中的 require 部分_**，重新运行安装依赖
