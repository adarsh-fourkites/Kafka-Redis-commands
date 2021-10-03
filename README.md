# Kafka-commands

cd kafka_2.13-2.6.0

 ./bin/zookeeper-server-start.sh config/zookeeper.properties
 
 ./bin/kafka-server-start.sh config/server.properties
 
 ### list
 bin/kafka-topics.sh --list --zookeeper localhost:2181  
 
### create
bin/kafka-topics.sh --create --topic topicname --bootstrap-server localhost:9092
 
### producer
bin/kafka-console-producer.sh --topic topicname --bootstrap-server localhost:9092

### describe
bin/kafka-topics.sh --describe --topic quickstart-events --bootstrap-server localhost:9092

### consumer 
bin/kafka-console-consumer.sh --topic quickstart-events --from-beginning --bootstrap-server localhost:9092


# Redis-commands

redis-cli

keys *

HGETALL Courier::something::dev

del Courier::something::dev



