# Basic Information

|      |      |
|------|------|
| Name | alibaba |
| Language | .java |
| Code Path | WeFe/common/java/common-data-storage/src/main/java/com/alibaba |
| Package Name | docs.common.java.common-data-storage.src.main.java.com.alibaba |
| Brief Description | DruidAbstractDataSource is the abstract base class of the Druid connection pool, implementing the DataSource interface and JMX management capabilities. It defines the core configuration parameters of the connection pool, including connection count control (initialSize/maxActive/minIdle), timeout settings (maxWait), validation queries (validationQuery), idle detection (timeBetweenEvictionRunsMillis), and more. It supports features such as filter chains, SQL monitoring, and connection leak detection, while tracking connection and statement execution statistics through atomic variables. |

# Description

DruidAbstractDataSource is an abstract class that implements the DruidAbstractDataSourceMBean, DataSource, DataSourceProxy, and Serializable interfaces. Serving as the core base class for the Druid connection pool, it encapsulates a wide range of connection pool configuration parameters and runtime state metrics. Key features include: connection pool size control (initialSize/maxActive/minIdle), connection acquisition timeout (maxWait), connection validity detection (validationQuery/testWhileIdle), idle connection reclamation policies (timeBetweenEvictionRunsMillis/minEvictableIdleTimeMillis), monitoring statistics (executeCount/commitCount/rollbackCount), filter mechanism (filters), and abnormal connection handling (exceptionSorter). The class defines the core processes for connection creation, destruction, and validation, ensuring thread safety through atomic variables and lock mechanisms. It also supports JMX monitoring, providing extensive runtime statistical information. Subclasses are required to implement specific connection pool management logic.


### Package Internal Structure View

```mermaid
graph TD
    alibaba --> druid
    druid --> pool
    pool --> DruidAbstractDataSource.java
```

This flowchart illustrates the complete hierarchical relationship from alibaba to DruidAbstractDataSource.java. The path starts from the top-level directory alibaba, extends downward to the druid subdirectory, then proceeds into the pool subdirectory, and finally reaches the specific Java source file DruidAbstractDataSource.java. The entire structure clearly presents the four-level directory containment relationship, conforming to Mermaid format requirements with standardized node naming.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [druid](druid/_module.md) | package | DruidAbstractDataSource is the abstract base class of the Druid connection pool, implementing the DataSource interface and JMX management capabilities. It defines the core configuration parameters of the connection pool, including connection count control (initialSize/maxActive/minIdle), timeout settings (maxWait), validation queries (validationQuery), idle detection (timeBetweenEvictionRunsMillis), and more. It supports features such as filter chains, SQL monitoring, and connection leak detection, and uses atomic variables to track connection and statement execution statistics. |


