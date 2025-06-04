```
export OPENAI_API_KEY="my_key"
```

Running ElasticSearch:
```commandline
docker run -it \
  --rm \
  --name elasticsearch \
  -p 9200:9200 \
  -p 9300:9300 \
  -e "discovery.type=single-node" \
  -e "xpack.security.enabled=false" \
  -e "ES_JAVA_OPTS=-XX:-UseContainerSupport -Xms2g -Xmx2g" \
  -e "JAVA_TOOL_OPTIONS=-XX:-UseContainerSupport" \
  --memory="4g" \
  docker.elastic.co/elasticsearch/elasticsearch:9.0.1
```