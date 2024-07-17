---
title: About Kafka Borkers
date: 2024-07-16 22:11 +0300
categories: [Kafka]
tags: [Kafka, Brokers]
author: Ramar Periyaraju
---

### Kafka Brokers

- **Cluster Composition**:

  - A Kafka cluster is composed of multiple brokers (servers).
  - Each broker is identified by a unique ID.
  - Each broker contains certain topic partitions.

- **Connection Mechanism**:

  - Connecting to any broker (called a bootstrap broker) gives access to the entire cluster.
  - Kafka clients use smart mechanisms to handle connections across the cluster.

- **Cluster Size**:
  - A good starting point is 3 brokers, but large clusters can have up to 100 brokers.
