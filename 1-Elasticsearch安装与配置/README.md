##### 启动单节点

```
./elasticsearch -E node.name=node0 -E cluster.name=geektime -E path.data=node0_data
```

##### 安装插件

```
./elasticsearch-plugin install analysis-icu
```

##### 查看插件

```
./elasticsearch-plugin list
```

##### 查看安装的插件

```\
GET http://localhost:9200/_cat/plugins?v
```

##### Start multi-nodes Cluster

```
./elasticsearch -E node.name=node0 -E cluster.name=geektime -E path.data=node0_data
./elasticsearch -E node.name=node1 -E cluster.name=geektime -E path.data=node1_data
./elasticsearch -E node.name=node2 -E cluster.name=geektime -E path.data=node2_data
./elasticsearch -E node.name=node3 -E cluster.name=geektime -E path.data=node3_data
```

##### 查看集群

```
GET http://localhost:9200
```

##### 查看nodes

```
GET _cat/nodes
GET _cluster/health
```

## 相关阅读

- <https://www.elastic.co/guide/en/elasticsearch/reference/current/install-elasticsearch.html>
- <https://www.elastic.co/guide/en/elasticsearch/reference/current/settings.html>
- <https://www.elastic.co/guide/en/elasticsearch/reference/current/important-settings.html>
- Elasticsearch on Kuvernetes <https://www.elastic.co/cn/blog/introducing-elastic-cloud-on-kubernetes-the-elasticsearch-operator-and-beyond>
- CAT Plugins API <https://www.elastic.co/guide/en/elasticsearch/reference/7.1/cat-plugins.html>

