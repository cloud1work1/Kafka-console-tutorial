# Kafka-console-tutorial (Assuming windows OS)
- ## Kafka Zookeeper Start
  bin\zookeeper-server-start.bat ..\\..\config\zookeeper.properties
- ## Kafka Server Start
  bin\kafka-server-start.bat ..\..\config\server.properties
- ## Create topic with single replication and load factor
  bin\kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic &lt;topic-name&gt;
- ## Create Producer
  bin\kafka-console-producer.bat --broker-list localhost:9092 --topic &lt;topic-name&gt;
  - Post Message
- ## Create Consumer 
  bin\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic &lt;topic-name&gt; --from-beginning
  - All the messages post from producer will be visible
