#### Docker 中运行 Elasticsearch

##### 启动

```
docker-compose up
```

##### 停止容器

```
docker-compose down
```

##### 停止容器并移除数据

```
docker-compose down -v
```

##### Docker 常用命令

```
# 查看所有镜像
docker images
# 查看运行中的所有容器
docker ps -a
# 停止、启动、杀死、重启
docker stop <name/id>
docker start <name/id>
docker kill <name/id>
docker restart <name/id>
# 删除容器
docker rm <name/id>
# 查看容器IP
docker inspect -f='{{.Name}} {{.NetworkSettings.IPAddress}} {{.HostConfig.PortBindings}}' $(docker ps -aq)
# 进入启动中的容器
docker exec -ti <容器名> /bin/bash
# 查看容器日志
docker logs -t -f --tail 10 <容器名>
# 复制容器中的文件
docker cp <容器ID>:<要复制的容器中的文件路径> <宿主机目标路径>
# 复制主机文件到容器
docker cp <宿主机目标路径> <容器ID>:<要复制的容器中的文件路径>
# docker volume
# 查看、创建、删除 volume
docker volumen ls
docker volumen create <name>
docker volumen rm <namme>
```

## 相关阅读

- 安装docker https://www.docker.com/products/docker-desktop
- 安装 docker-compose https://docs.docker.com/compose/install/
- 如何创建自己的Docker Image - https://www.elastic.co/cn/blog/how-to-make-a-dockerfile-for-elasticsearch
- 如何在为docker image安装 Elasticsearch 插件 - https://www.elastic.co/cn/blog/elasticsearch-docker-plugin-management
- 如何设置 Docker 网络 - https://www.elastic.co/cn/blog/docker-networking
- Cerebro 源码 https://github.com/lmenezes/cerebro
- 一个开源的 ELK（Elasticsearch + Logstash + Kibana） docker-compose 配置 https://github.com/deviantony/docker-elk