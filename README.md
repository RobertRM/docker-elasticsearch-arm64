# Docker Elasticsearch form ARM64 
Dockerfile for Elasticsearch that runs on ARM64

## How to Use
```
git clone https://github.com/RobertRM/docker-elasticsearch-arm64 && cd docker-elasticsearch-arm64
docker-compose up
```
Wait a bit for it to start up then run (Replace `localhost` with the IP of your server if you're checking remotely)
```
curl -X GET "localhost:9200/_cat/nodes?v&pretty""
```
You should get something back like this
```
ip       heap.percent ram.percent cpu load_1m load_5m load_15m node.role  master name
10.0.4.2           42          59  27    1.33    0.56     0.42 cdhilmrstw *      elasticsearch
```

## Build Image For Use
Use the bash script:
```
sh ./build_image.sh
```
or build directly
```
docker build -t robertrm/docker-elasticsearch-arm64:7.10.1 .
```
