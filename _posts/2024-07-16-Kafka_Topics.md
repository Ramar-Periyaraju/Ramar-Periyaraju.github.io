---
title: About Topics in Kafka
date: 2024-07-16 22:11 +0300
categories: [Kafka]
tags: [Kafka, Topics]
author: Ramar Periyaraju
---

# Topics, Partitions, and Offsets – Important Notes

## Overview

In Apache Kafka, a **topic** is a particular stream of data, similar to a table in a database. You can create as many topics as needed. Each topic is identified by a unique name, such as `logs`, `twitter_tweets`, or `trucks_gps`. The messages in a topic can be in any format, like JSON. The sequence of messages is referred to as a data stream.

Kafka topics are immutable, meaning once data is written to a partition, it cannot be changed.

## Partitions and Offsets

A topic is divided into partitions. For example, a topic can have 100 partitions. Messages within each partition are ordered, and each message receives a unique, incremental identifier called an **offset**.

Here are some key points to note:

- **Immutability**: Once data is written to a partition, it cannot be changed.
- **Data Retention**: Data is retained only for a limited time (default is one week, but this can be configured).
- **Partition-specific Offsets**: Offsets are specific to each partition. For instance, offset 3 in partition 0 is different from offset 3 in partition 1. Offsets are not reused, even if previous messages are deleted.
- **Order Guarantee**: Order is guaranteed only within a partition, not across partitions.
- **Data Assignment**: Data is assigned to partitions randomly unless a key is provided.

## Example Use Case: GPS Tracking for a Fleet of Trucks

Imagine you have a fleet of trucks, and each truck reports its GPS position to Kafka every 20 seconds. Each message contains the truck ID and its position (latitude and longitude).

You could create a topic named `trucks_gps` that contains the position of all trucks. Suppose this topic is created with 10 partitions. Once the topic is created, you can display the data on a location dashboard.

This setup allows you to efficiently manage and process the GPS data from all the trucks, leveraging Kafka's partitioning and offset mechanisms to handle large volumes of data and ensure the order within partitions.

### Topics, Partitions, and Offsets - Important Notes

1. **Immutability of Data**: Once data is written to a partition, it cannot be changed. This ensures data integrity and consistency.
2. **Data Retention**: Data is kept for a limited time (default is one week, configurable). This helps manage storage and maintain performance.
3. **Partition-Specific Offsets**: Offsets only have meaning within their specific partition. For example, offset 3 in partition 0 does not represent the same data as offset 3 in partition 1. Offsets are unique and never reused, even if previous messages are deleted.
4. **Guaranteed Order Within Partitions**: Order is guaranteed only within a partition and not across partitions. This means that messages in a partition will be read in the order they were written.
5. **Random Data Assignment**: Data is assigned randomly to partitions unless a key is provided, which allows for more control over data distribution.

### Example Scenario

- **Fleet of Trucks**: Suppose you have a fleet of trucks, and each truck reports its GPS position to Kafka every 20 seconds. Each message contains the truck ID and its position (latitude and longitude).
- **Kafka Topic**: Create a topic named `trucks_gps` to contain the positions of all trucks, with 10 partitions.
- **Dashboard Display**: Once the topic is created, you can display the location data on a dashboard.
