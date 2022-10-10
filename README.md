# docker-compose-kafka
https://developer.confluent.io/quickstart/kafka-docker/
## Create Topic
```
docker exec broker kafka-topics --bootstrap-server broker:9092 --create --topic quickstart
```
## List the topics
```
docker exec broker kafka-topics --bootstrap-server broker:9092 --list
```
## Write messages to the topic
### Without key
```
docker exec --interactive --tty broker kafka-console-producer --bootstrap-server broker:9092 --topic quickstart
```
### With key
```
docker exec --interactive --tty broker kafka-console-producer --bootstrap-server broker:9092 --topic quickstart --property "key.separator=-" --property "parse.key=true"
```
## Read messages from the topic
### Without key
```
docker exec --interactive --tty broker kafka-console-consumer --bootstrap-server broker:9092 --topic quickstart --from-beginning
```
### With key
```
docker exec --interactive --tty broker kafka-console-consumer --bootstrap-server broker:9092 --topic quickstart --from-beginning --property "key.separator=-" --property "print.key=true"
```
