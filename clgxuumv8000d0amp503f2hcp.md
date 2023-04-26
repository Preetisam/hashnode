---
title: "Microservices Architecture Asynchronous communication"
seoTitle: "Microservices Architecture Asynchronous"
seoDescription: "In a microservices architecture, each service should be responsible for one specific task, which means that each service can operate independently"
datePublished: Wed Apr 26 2023 15:32:44 GMT+0000 (Coordinated Universal Time)
cuid: clgxuumv8000d0amp503f2hcp
slug: microservices-architecture-asynchronous-communication
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/MNd-Rka1o0Q/upload/8c933c52294728ca589166aa6dffe8e9.jpeg
tags: asynchronous, communication, microservices-architecture

---

Microservices architecture is designed to support the development and deployment of small, independent services that work together to provide a complete system. In such an architecture, asynchronous communication is commonly used to achieve a decoupled and scalable system.

In a microservices architecture, each service should be responsible for one specific task, which means that each service can operate independently and asynchronously from other services. To achieve asynchronous communication, there are two popular patterns used in microservices architecture:

event-driven architecture and message-based communication.

1. **Event-driven architecture (EDA)**: In EDA, a service emits an event after it completes an operation, so other services can listen to this event and react accordingly. Events can be sent through message brokers such as Apache Kafka, RabbitMQ, or AWS Kinesis. This pattern enables services to communicate asynchronously without being tied to the response time of other services.
    
2. **Message-based communication:** In message-based communication, a sender service sends a message to a message broker, which then distributes the message to the relevant recipient services. The recipient services receive the message and process it, and may send a response message back to the sender. This pattern is also used for asynchronous communication as it allows services to operate independently of each other.
    

In summary, microservices architecture uses asynchronous communication patterns such as event-driven architecture and message-based communication to enable decoupled and scalable systems. These communication patterns allow services to communicate with each other without blocking or waiting for a response, thus improving the overall system's resilience and scalability.