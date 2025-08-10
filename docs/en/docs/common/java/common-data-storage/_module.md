# Basic Information

|      |      |
|------|------|
| Name | common-data-storage |
| Language | .java |
| Code Path | WeFe/common/java/common-data-storage |
| Package Name | docs.common.java.common-data-storage |
| Brief Description | DruidAbstractDataSource is the core abstract class of the Druid connection pool, providing fundamental functionalities such as connection pool configuration, monitoring, and thread safety. The multi-cloud storage module supports unified operations across heterogeneous databases, including capabilities like sharding, pagination, and stream processing, and relies on mainstream cloud SDKs and JDBC drivers. |

# Description

## Overview  
The core responsibility of this module is to enable unified data storage and management across cloud platforms and multiple databases, integrating connection pool control and dynamic sharding capabilities. DruidAbstractDataSource serves as the base class for the connection pool, providing thread-safe configurations (e.g., maxActive for connection limit control) and JMX monitoring. The data storage module encapsulates CRUD operations and paginated queries, resembling the adapter pattern. Key data structures include sharding strategies, connection configurations (e.g., ClickhouseConfig), and generic key-value pairs. External dependencies include the Druid connection pool, cloud platform SDKs (Alibaba Cloud/Tencent Cloud), and JDBC drivers. For instance, Druid uses testWhileIdle to validate connection integrity, while the data module employs hashKeyToPartition for dynamic sharding.  

## Key Business Scenarios  
The module is designed for hybrid cloud storage and heterogeneous database scenarios. A typical workflow involves configuration initialization → sharding/serialization → multi-threaded or stream processing → monitoring callbacks. The Druid connection pool supports high-concurrency request management, while the data module provides paginated queries (e.g., PageInputModel) and key-value storage (e.g., DataItemModel). The interaction model is configuration-driven—for example, Alibaba Cloud OTS uses hash partitioning, and MySQL queries via pagination parameters. Integration cases span from Druid connection pool initialization to getByStream stream processing, delivering an end-to-end data solution.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | DruidAbstractDataSource is the core abstract class of the Druid connection pool, providing foundational functionalities such as connection pool configuration, monitoring, and thread safety. The multi-cloud storage module supports unified operations across heterogeneous databases, including capabilities like sharding, pagination, and stream processing, and relies on mainstream cloud SDKs and JDBC drivers. |


