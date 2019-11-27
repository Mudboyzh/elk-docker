## elk-docker
Elasticsearch cluster 

#### Node Type

| Node Name | Node Type     | Node Port |
| ----------| ------------- | --------- |
| Node 1    | Master / Data |   9200    |
| Node 2    | Master only   |   9202    |
| Node 3    | Master / Data |   9203    |


#### Start

1. `cd /path/to/elk-docker`
2. `docker-compose up -d`