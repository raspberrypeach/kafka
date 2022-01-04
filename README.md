# kafka

# kafka start(background)
sudo sh bin/kafka-server-start.sh -daemon config/server.properties 

# create topic
($kafka_path/bin)
sudo sh ./kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 2 --partitions 10 --topic ${TOPIC_NAME}


# inquiry topic
sudo sh ./kafka-topics.sh --list --bootstrap-server localhost:9092

# inquiry topic(detail)
sudo sh ./kafka-topics.sh --describe --bootstrap-server localhost:9092 --topic ${TOPIC_NAME}
