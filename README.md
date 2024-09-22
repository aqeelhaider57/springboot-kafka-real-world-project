#Kafka configuration
1 - download kafka latest version and follow given instruction
2 - config zookeeper.properties with path and server.properties set path -> two properties file 
	Kafka folder contain config folder config -> zookeeper.properties and server.properties
	server.properties -> log.dirs=C:/kafka/kafka-logs
	zookeeper.properties -> dataDir=c:/kafka/zookeeper-data
 - cmd kafka folder
3 - start Zookeeper and then start kafka
	1 - cmd run kafka folder => c:\kafka> .\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
	2 - cmd run kafka folder => c:\kafka> .\bin\windows\kafka-server-start.bat .\config\server.properties

4 - topic -> then create topic and kafka default port is 9092
	c:\kafka\bin\windows>kafka-topics.bat --create --bootstrap-server localhost:9092 --topic test

5 - Producer -> kick off producer function to produce data
	cmd -> c:\kafka\bin\windows>kafka-console-producer.bat --broker-list localhost:9092 --topic test

6 - consumer ->
	cmd -> c:\kafka\bin\windows>kafka-console-consumer.bat --topic test --bootstrap-server localhost:9092 --from-beginning

7 - data -> producer data input data to producer
	{"Name: "Your Name", "Age":"20", "Gender":"Male"}

