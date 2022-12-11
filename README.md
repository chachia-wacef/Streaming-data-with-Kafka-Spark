# Streaming-data-with-Kafka-Spark

++Useful Commands to execute the project on windows 

STEP 1: START THE KAFKA ENVIRONMENT
# Start the ZooKeeper service
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties

# Start the Kafka broker service
.\bin\windows\kafka-server-start.bat .\config\server.properties

STEP 2: CREATE A TOPIC TO STORE YOUR EVENTS
.\bin\windows\kafka-topics.bat --create --topic waceftopic --bootstrap-server localhost:9092

# To test the kafka topic

STEP 3: WRITE SOME EVENTS INTO THE TOPIC x
.\bin\windows\kafka-console-producer.bat --topic waceftopic --bootstrap-server localhost:9092

STEP 4:  READ THE EVENTS
.\bin\windows\kafka-console-consumer.bat --topic waceftopic --from-beginning --bootstrap-server localhost:9092

# Delete the topic to excute the java code properly, The reexecute step 2
.\bin\windows\kafka-topics.bat --zookeeper localhost:9092 --delete --topic waceftopic
