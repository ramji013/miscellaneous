# Kafka


It is distributed streaming platform. Communication between single producing and consumer system is easy but challenges come when there are multiple producer and multiple consumer system. in the way of
1. how the data can be communicated, i.e. http, tcp, jdbc, etc...
2. data format (csv, xl, .txt, .json, etc..)


Apache kafka decouple between data stream. The target system will get the data directly from kafka.


<img width="1005" alt="image" src="https://user-images.githubusercontent.com/5616261/114283774-1394ae80-9a7e-11eb-8761-b6ba52b16171.png">


## Why Apache kafka

1. it was created by linkedin and maintained by private firm confluent
2. it is distributed, resilient architecture, fault tolerent
3. It scales horizontally upto 100 brokers and it process millions of messages per second
4. High performance, it process data less than 10ms


## Use cases of kafka:

1. messaging system
2. activity tracking
3. gather metrices from many different locations (IoT device)
4. Application log gathering
5. stream processing
6. decoupling of system dependencies
7. Integration with bigdata technologies


# Architecture

Producer push messages to kafka cluster where it has multiple brokers which is nothing but multiple instances of kafka servers which has the topic. The consumer will pull the message from the topic.

Zookeeper is broker configure environment.


<img width="569" alt="image" src="https://user-images.githubusercontent.com/5616261/114291858-44480880-9abd-11eb-9fc5-0bf18530ae62.png">


Why Kafka and why not JMS:

1. Kafka ensures that the messages are received in the order in which they were sent at the partition level. JMS doesnt have such contracts.
2. Filtering mechanism not applicable for kafka, the consumer system should take care of it
3. Kafka brokers store the messages for a specific period of time irrespective of whether the message is picked up by consumer or not, where JMS provides in-memory or disk based storage of messages.
