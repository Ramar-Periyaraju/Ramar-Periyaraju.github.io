---
title: About Producers in Kafka
date: 2024-07-2016 22:11 +0300
categories: [Kafka]
tags: [Kafka, Producers]
author: Ramar Periyaraju
---

### Producers: Message Keys

1. **Sending a Key with a Message**:
   - Producers can choose to send a key with a message. The key can be of various types, such as a string, number, or binary.
   - **Null Key**: If the key is null, the data is sent in a round-robin fashion to any partition.
   - **Non-Null Key**: If the key is not null, all messages for that key will always go to the same partition. This is achieved through hashing.
   - **Use Case**: Keys are typically used when message ordering for a specific field is required (e.g., `truck_id`).

### Kafka Message Serialization

1. **Message Creation**: Messages are created by the producer.
2. **Kafka Message Serializer**:
   - **Function**: The serializer accepts bytes as input from producers and sends bytes out as output to consumers.
   - **Serialization**: This process involves transforming objects/data into bytes. Serialization is applied to both the value and the key.
   - **Common Serializers**:
     - String
     - Integer, Float
     - Avro
     - Protobuf

### Kafka Message Key Hashing

1. **Partition Logic**: A Kafka partitioner is code logic that determines which partition a record is sent to.
2. **Key Hashing**: This process maps a key to a partition. By default, Kafka uses the `murmur2` algorithm for hashing keys.
3. **Formula**: targetPartition = Math.abs(Utils.murmur2(keyBytes)) % (numPartitions - 1)

This formula helps in evenly distributing messages across the partitions, ensuring efficient use of resources and balanced load distribution.
