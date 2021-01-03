# docker-zipkin-nginx-example
This is the example for docker-zipkin-nginx project: https://github.com/geekeren/docker-zipkin-nginx


## How to run?
```
docker-compose up
```
Then open http://localhost at browser, you can see logs in the console:


```
zipkin-nginx_1  | traceId=e8379cbb3ef9e7d0 spanId=a1372cff03c1a734 
```


docker run -d -p 9411:9411 --name zipkin-gcp \
  -e STORAGE_TYPE=stackdriver \
  -e GOOGLE_APPLICATION_CREDENTIALS=/zipkin/.gcp/credentials.json \
  -e STACKDRIVER_PROJECT_ID=analog-pilot-296718 \
  -v $HOME/.gcp:/zipkin/.gcp:ro \
  openzipkin/zipkin-gcp



  docker run -d -p 9411:9411 openzipkin/zipkin


  {
  "service_name": "zipkin-nginx",
  "collector_host": "host.docker.internal",
  "collector_port": 9411
}