# Kafka

### Main Idea
Databases store object 'state' info. Logs store event state information, ordered sequence of event states. Logs much more scalable versus database.
Kafka calls these logs 'topics'. Kafka is essentially a topic management system, an event streaming platform. Topics are stored in a durable way, can be small or large, can work short or long term. 

### Services Communication
There are streams of services that consume or feed/produce to Kafka topics at any time. In this way, Kafka is somewhat of an intermediary, allows services to talk to each other via the occurrence of events. 

### Integration with Database
Kafka connect helps connect data from old databases to new topics, or from old systems to new ones, etc. Can also group, integrate, enrich, or have data from one Kafka topic to other topics. 

### Kafka Streams
Basis of event streaming - as real-time data from event sources is extracted, Kafka allows for the processing or general reacting to this data/event stream 

### Fault Tolerance
Distributed architecture of Kafka ensures that if any one system fails, the overall work and operation goes on without a hitch. Topics are also replicated across regions, hence multiple brokers have copes if your data (brokers are the servers from the storage layer that hold the Kafka clusters). Topics are also partitioned into different buckets given to different brokers, allows reading/writing from many brokers at the same time and is thus more scalable. 