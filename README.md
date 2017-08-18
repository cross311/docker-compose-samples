# docker-compose-samples
Collection of docker compose yml files to help test cool technology

## Kafka
Docker compose spotify's single container for both zookeeper and kafka, auto configured.
additionally running kafka-manager from `dockerkafka`

### Run platform
```sh
wget -q -O - https://raw.githubusercontent.com/cross311/docker-compose-samples/master/kafka-docker-compose.yml | docker-compose -f - -p expressUp up -d
```

### Initialize
I have not been able to determine how to get the kafka-manager to auto pick up the cluster.
Follow these steps to register the kafka docker instance with the manager.

 - `http://localhost:9000/addCluster`
 - Give it a name (example: `docker-kafka`)
 - Cluster host: `zookeeper:2181`
 - kafka version: `0.8.2.1`
 - Spotify's version does not support JMX :(
 - Save!
