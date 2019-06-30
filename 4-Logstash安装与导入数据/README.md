##### 

##### Logstash 安装，并导入Movielens测试数据集

- 600个用户将100,000个评级和3,600个标签应用程序应用于9,000部电影。 上次更新时间：9/2018。
- movielens/ml-latest-small/movies.csv movie数据
- movielens/logstash.conf //logstash 7.x 配置文件，
- movielens/logstash6.conf //logstash 6.x 配置文件

##### 下载与ES相同版本Logstash（7.2.0），并解压到相应目录

##### 修改/logstash-7.2.0/config/logstash.conf

##### 指定配置文件启动

```
./logstash -f YOUR_PATH/logstash.conf
```

#### 相关阅读

- 下载最MovieLens最小测试数据集：https://grouplens.org/datasets/movielens/
- Logstash下载：https://www.elastic.co/cn/downloads/logstash
- Logstash参考文档：https://www.elastic.co/guide/en/logstash/current/index.html

