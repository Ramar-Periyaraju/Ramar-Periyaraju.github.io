---
title: About AWS Aurora ?
date: 2024-07-15 21:00 +0300
categories: [AWS]
tags: [Aurora, Database]
author: Ramar Periyaraju
---

# Amazon Aurora: AWS's Proprietary Database Service

## Overview

Amazon Aurora is a high-performance, cloud-optimized relational database service offered by AWS. It is compatible with both PostgreSQL and MySQL, allowing applications to use the same drivers as they would with a native PostgreSQL or MySQL database.

## Key Features

- **Performance**: AWS claims that Aurora offers up to 5x the performance of MySQL and up to 3x the performance of PostgreSQL. This is achieved through various optimizations specifically designed for the cloud environment.

- **Read Replicas**: Aurora supports up to 15 read replicas, with replication lag typically under 10 milliseconds, making it significantly faster than MySQL.

- **Failover and High Availability**: Aurora offers native high availability with instant failover. In the event of a failure, the failover process is automated and typically completes in less than 30 seconds. This ensures minimal disruption to your applications.

- **Cost**: Aurora is approximately 20% more expensive than standard RDS offerings. However, this cost increase comes with significant performance and availability benefits.

## High Availability and Read Scaling

- **Data Replication**: Aurora maintains 6 copies of your data across 3 Availability Zones (AZs). For any write operation, 4 out of the 6 copies must acknowledge the write, while 3 out of the 6 copies are required for read operations. This architecture ensures data durability and availability.

- **Self-Healing**: Aurora employs a self-healing storage system with peer-to-peer replication, automatically detecting and repairing any faults.

- **Storage Architecture**: Data is striped across hundreds of volumes, ensuring high performance and durability.

## Scalability

- **Write and Read Instances**: Aurora allows a single instance to handle write operations. In the event of a failure, automated failover promotes a read replica to become the new master, typically within 30 seconds. Aurora supports up to 15 read replicas to distribute read traffic.

- **Cross-Region Support**: Aurora supports cross-region replication, enhancing disaster recovery capabilities and enabling globally distributed applications.

- **Auto-Expanding Storage**: Aurora's storage automatically expands from 10GB to 128TB as needed, eliminating the need for manual scaling.

## Additional Features of Aurora

- **Automatic Failover**: Ensures high availability and minimal downtime by automatically failing over to a standby instance in the event of a failure.

- **Backup and Recovery**: Provides automated backup and recovery options to protect your data.

- **Isolation and Security**: Offers robust isolation and security features to protect your data.

- **Industry Compliance**: Complies with various industry standards to meet regulatory requirements.

- **Push-Button Scaling**: Allows for easy and quick scaling of resources to meet changing demands.

- **Automated Patching with Zero Downtime**: Applies patches and updates automatically without causing any downtime.

- **Advanced Monitoring**: Provides comprehensive monitoring tools to track performance and health.

- **Routine Maintenance**: Handles routine maintenance tasks automatically.

- **Backtrack**: Allows you to restore your data to any point in time without using backups.

## Conclusion

Amazon Aurora is a powerful, cloud-optimized database service that offers significant performance improvements and high availability compared to traditional RDS offerings. With features like rapid failover, extensive read replicas, automatic scaling, and robust security, Aurora is an excellent choice for applications requiring robust performance and reliability.
