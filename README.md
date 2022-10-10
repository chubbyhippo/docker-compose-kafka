# docker-compose-kafka
https://developer.confluent.io/quickstart/kafka-docker/
## Create Topic
```
docker exec broker kafka-topics --bootstrap-server broker:9092 --create --topic quickstart
```
## Write messages to the topic
```
docker exec --interactive --tty broker kafka-console-producer --bootstrap-server broker:9092 --topic quickstart
```
## Read messages from the topic
```
docker exec --interactive --tty broker kafka-console-consumer --bootstrap-server broker:9092 --topic quickstart --from-beginning
```
