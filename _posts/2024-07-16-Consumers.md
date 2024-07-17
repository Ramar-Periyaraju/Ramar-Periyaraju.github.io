---
title: About Consumers in Kafka
date: 2024-07-16 22:11 +0300
categories: [Kafka]
tags: [Kafka, Consumers]
author: Ramar Periyaraju
---

### Consumers: (Pull)

1. **Reading Data**:

   - Consumers read data from a topic identified by its name.
   - They automatically know which broker to read from.
   - In case of broker failures, consumers know how to recover.
   - Data is read in order from low to high within each partition.

2. **Consumer Deserializer**:

   - Indicates how to transform bytes into objects/data.
   - Used on both the value and the key of the message.
   - **Common Deserializers**:
     - String
     - Integer, Float
     - Avro
     - Protobuf

3. **Important Note**:
   - Serialization and deserialization types must not change during a topic's lifecycle. If changes are needed, create a new topic instead.
