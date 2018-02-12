---
layout: post
title: registry install
date: 2018-02-11 14:44:00 +0300
description: 
tag: [docker]
---

1、启动registry
~~~ shell
docker run -d -v /data/registry:/var/lib/registry -p 5000:5000 --restart=always --name registry registry
~~~
> Registry服务默认会将上传的镜像保存在容器的/var/lib/registry，我们将主机的/data/registry目录挂载到该目录，即可实现将镜像保存到主机的/data/registry目录了。

2、启动registry-ui
~~~ shell
docker run -d -p 8080:8080 --name registry-ui atcol/docker-registry-ui
~~~