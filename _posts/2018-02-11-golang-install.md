---
layout: post
title: golang install
date: 2018-02-11 14:44:00 +0300
description: golang install.
---

1、参照Go官网，找到linux版本下载路径，执行以下操作下载Go语言包
~~~ shell
curl -O https://storage.googleapis.com/golang/go1.8.3.linux-amd64.tar.gz
~~~

2、解压go1.8.3.linux-amd64.tar.gz至/usr/local目录下，执行如下操作：
~~~ shell
tar -C /usr/local -xzf go1.8.3.linux-amd64.tar.gz
~~~

3、配置go环境变量

修改/etc/profile文件使其永久性生效，并对所有系统用户生效，在文件末尾加上如下两行代码
~~~ shell
export PATH=$PATH:/usr/local/go/bin
export GOPATH=/opt/gopath
~~~

执行修改后，继续执行：
~~~ shell
source profile
~~~

使其修改生效。随后可通过下述命令：
~~~ shell
echo $PATH
~~~

查看是否添加成功。

最后可通过
~~~ shell
go version
~~~
查看当前go版本信息，正常情况下返回安装go的版本信息。