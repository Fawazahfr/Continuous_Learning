# Amazon Web Services
Category: Cloud Computing Service

## TOC
[Purposes](#purposes)  
    - [Large and Easy](#large-and-easy)  
    - [AMIs](#amis)  
    - [Autoscaling](#autoscaling)  
    - [Load Balancing](#load-balancing)  
    - [Multiple Physical Centers](#multiple-physical-centers)
    - [Security](#security)  
    - [Database Support](#database-support)  
    - [S3 Storage](#s3-storage)  
    - [Caching](#caching)  


## Purposes

### Large and Easy
Large computing capacity without needing to maintain it yourself; Amazon takes care of all maintenance. 

### AMIs
Amazon Machine Images, VM configurers that essentially allow the loading of diff kinds of apps in an 'instance'. Users can create, delete, and manage instances as they desire, you can launch as many instances off of an AMI as you want. 

### Autoscaling
AWS scales up and down servers as needed for an application, such that servers are never overloaded, and that there is not too much fluff space that is unused. Load balancing means that incoming traffic is distributed evenly through these different servers. 

### Load Balancing
Has general distribution for the app that gets user traffic based on diff servers, but there is also Application Load balancing which routes traffic based on the content or needs of the application or the user access.

### Multiple Physical Centers
In case of servers going down or disaster recovery, the deployment of the AWS servers across multiple physical locations ensures that your application stays live, and it won't be a DB center physical issue that brings it down.

### Security
Advanced ecryption in communication between servers and instances, as well as each instance having its own security groups with constrained communication. 

### Database Support
**RDS - Relational Database Service:** Allows easy setup, operation, and scaling of popular SQl databases on the cloud. Once again, leaves more tedious DB management to AWS so you can worry less.

**DynamoDB - NoSQL cloud database:** Also very easy and scaleable, allows for maximally minimal latency and supports both document and key-value storage models. 

### S3 Storage
Massive and inexpensive storage payed for monthly, secure storage infrastructure.

### Caching
Elasticache works with Redis and Memchached to provide extremely quick data access and retrieval that works with most systems, allowing focus on in-memory data stores rather than slower disk based counterparts.


