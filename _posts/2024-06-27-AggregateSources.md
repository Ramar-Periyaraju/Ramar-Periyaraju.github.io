---
title: About Aggregate Sources in Pega
date: 2024-06-27 20:11 +0300
categories: [Pega, Pega Platform]
tags: [Pega, Data Pages, Aggregate Sources]
author: Ramar Periyaraju
---

## About Aggregate Sources

Aggregate Sources in Pega data pages allow you to combine data from multiple sources to populate a single data page. This feature offers several advantages:

1. **Introduction in Pega 8.4**: Aggregate Sources became available as a data page source option starting from Pega version 8.4.

2. **Simplified Data Integration**: You can aggregate data from various sources like REST connectors, databases, or activities into a single data page, eliminating the need for complex activities to merge data.

3. **Improved Performance**: By loading data from multiple sources simultaneously, aggregate sources can potentially improve the overall performance and loading speed of your data pages.

4. **Flexibility**: You can mix and match different types of data sources (e.g., REST connectors, database lookups, activities) within the same data page, providing greater flexibility in data retrieval.

5. **Ordered Execution**: Sources are executed in the order they are configured, allowing you to control the sequence of data retrieval.

6. **Conditional Sourcing**: When using multiple sources, you can configure logical conditions for each source to determine whether to query that particular data source. This allows for more dynamic and context-aware data retrieval.

7. **Easier Maintenance**: Instead of managing multiple data pages or complex activities, you can configure all data sources in one place, making it easier to maintain and update your data integration logic.

8. **Separation of Concerns**: Aggregate sources help maintain a clear separation between business processes and integration details, allowing developers to use sourced data without needing to know the specifics of each data source.

To use aggregate sources, select the "Aggregate sources" option on the data page rule form and then configure each data source individually. This feature is particularly useful when you need to combine data from different systems or APIs to create a comprehensive view of information within your Pega application.
