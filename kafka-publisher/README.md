

# Step1:
====
Start Zookeeper in window: go to installation dir like: D:\Kafka-Installation\kafka_2.12-2.3.0\bin\windows> and then 
fire zookeeper start command
D:\Kafka-Installation\kafka_2.12-2.3.0\bin\windows>zookeeper-server-start.bat D:\Kafka-Installation\kafka_2.12-2.3.0\config\zookeeper.properties

# Step2: Start Kafka server:

D:\Kafka-Installation\kafka_2.12-2.3.0\bin\windows>kafka-server-start.bat  D:\Kafka-Installation\kafka_2.12-2.3.0\config\server.properties

# Step3: Create topic:

D:\Kafka-Installation\kafka_2.12-2.3.0\bin\windows>kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 -topic kafkaTopic

** start the kafka application and push data by end point to the spaecific topic kafkaTopic

# Step4: fetch data from topic

D:\Kafka-Installation\kafka_2.12-2.3.0\bin\windows>kafka-console-consumer.bat --bootstrap-server  localhost:9092 --topic kafkaTopic
