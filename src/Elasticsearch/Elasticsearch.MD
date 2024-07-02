1. Run docker
```terminal
docker run -it \
    --rm \
    --name elasticsearch \
    -p 9200:9200 \
    -p 9300:9300 \
    -e "discovery.type=single-node" \
    -e "xpack.security.enabled=false" \
    -e "ES_JAVA_OPTS=-Xms1g -Xmx1g" \
    docker.elastic.co/elasticsearch/elasticsearch:8.4.3

```
2. test port forwarding:
```terminal
curl http://localhost:9200
```

3. stop the docker elastic search
```terminal
docker ps
```

```terminal
docker stop <container_id>
```

