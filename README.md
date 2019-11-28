## elk-docker
Elasticsearch cluster 
單主機叢集

#### Node Type

| Node Name | Node Type         | Node Port   |
| ----------| ----------------- | ----------- |
| Node 1    | Coordinating only | 9200 / 9300 |
| Node 2    | Master only       | 9202 / 9302 |
| Node 3    | Master / Data     | 9203 / 9303 |
| Node 3    | Master / Data     | 9203 / 9304 |


#### Start
1. Change your host ip in `discovery.seed_hosts`(elasticsearch-node-n.yml)
2. `cd /path/to/elk-docker`
3. `docker-compose up -d`
4. Open http://localhost:5601/myapp (Modify url prefix in kibana.yml if you need)