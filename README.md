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

redis-server #starts a redis server

redis-cli #command line

keys *  #display all keys

set key-name value #sets key

HGETALL Courier::something::dev

del key-name #deletes the key

flushall  #deletes all keys

clear #clears the cli

ttl key-name #returns time to live for that key, -1 never going to expire, -2 means already expired.

expire key-name time-in-seconds #sets the time to live.

setex key-name time-to-live value #sets the time to expire while setting the key-name to a value

### Lists in redis:

lpush array-name value1 value2 .. #pushing to the top/left of the array

rpush array-name value1 value2 .. #pushing to the right/bottom of the array

lrange array-name start(0) stop(-1) #print all values -1 means till the last element

lpop array-name #removes first element from top

rpop array-name #removes last element in array

### Sets in Redis:

sadd set-name value1 value2 #adding values to set

smembers set-name #prints all the values set has

srem set-name value #removes values from set-name

### hashes in Redis:

cannot have hashes inside hashes in redis.

hset hash-name key-name value 

hget hash-name key-name #returns the value

hgetall hash-name #returns all key names (odd nums) then values(even nums).

hdel hash-name #deletes all the properties

hexists hash-name key-name #bool if that hash exists






