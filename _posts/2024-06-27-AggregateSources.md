---
title: About Aggregate Source
date: 2024-06-27 20:11 +0300
categories: [Pega,Pega Platform}]
tags: [Pega, Pega Platform]
author: Ramar Periyaraju
---

What are Aggregate Sources and the advantage of Aggregate Source in Data page?

*1.Introduced in Pega 8.4: Aggregate Sources became available as a data page source option starting from Pega version 8.4
*2.Simplified Data Integration: You can aggregate data from various sources like REST connectors, databases, or activities into a single data page, eliminating the need for complex activities to merge data
*3.Improved Performance: By loading data from multiple sources simultaneously, aggregate sources can potentially improve the overall performance and loading speed of your data pages.
*4.Flexibility: You can mix and match different types of data sources (e.g., REST connectors, database lookups, activities) within the same data page, providing greater flexibility in data retrieval
*5.Ordered execution: Sources are executed in the order they are configured, allowing you to control the sequence of data retrieval.
*6.Conditional Sourcing: When using multiple sources, you can configure logical conditions for each source to determine whether to query that particular data source. This allows for more dynamic and context-aware data retrieval.
