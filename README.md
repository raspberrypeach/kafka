# kafka(v3.0.0) 

# kafka start(background)
sudo sh bin/kafka-server-start.sh -daemon config/server.properties 

# create topic
($kafka_path/bin)
sudo sh ./kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic ${TOPIC_NAME}

# producer-consumer test
sudo sh ./kafka-console-producer.sh --topic ${TOPIC_NAME} --bootstrap-server localhost:9092  
sudo sh ./kafka-console-consumer.sh --topic ${TOPIC_NAME} --from-beginning --bootstrap-server localhost:9092  

# inquiry topic
sudo sh ./kafka-topics.sh --list --bootstrap-server localhost:9092

# inquiry topic(detail)
sudo sh ./kafka-topics.sh --describe --bootstrap-server localhost:9092 --topic ${TOPIC_NAME}

# view topic
sudo sh ./kafka-console-consumer.sh --bootstrap-server localhost:9092 --from-beginning --topic ${TOPIC_NAME}
