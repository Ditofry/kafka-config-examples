## A Playground for configuring Kafka

### QuickStart
*Start ZooKeeper*
`zookeeper-server-start config/zookeeper.properties`

*Start Kafka*
`kafka-server-start config/server.properties`

*Create a topic*
`kafka-topics --zookeeper 127.0.0.1:2181 --topic kafka-security-topic --create --partitions 2 --replication-factor 1`

*Connect Producer*
`kafka-console-producer --broker-list localhost:9093 --topic kafka-security-topic --producer.config config/client.properties`

*Connect Consumer*
`kafka-console-consumer --bootstrap-server localhost:9093 --topic kafka-security-topic --from-beginning --consumer.config config/client.properties`
