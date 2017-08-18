# docker-compose-samples
Collection of docker compose yml files to help test cool technology

## Kafka
Docker compose spotify's single container for both zookeeper and kafka, auto configured.
additionally running kafka-manager from `dockerkafka`

```sh
wget -q -O - https://raw.githubusercontent.com/DockerKafka/docker-compose-samples/master/kafka-zookeeper-docker-compose.yml | docker-compose -f - -p expressUp up -d
```
