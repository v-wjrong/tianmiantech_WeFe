# Basic Information

|      |      |
|------|------|
| Name | data |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mysql/src/main/java/com/welab/wefe/common/data |
| Package Name | docs.common.java.common-data-mysql.src.main.java.com.welab.wefe.common.data |
| Brief Description | MyJpaRepository provides default methods for pagination queries and string processing. PageUtils handles pagination for single objects. The OrderBy enum defines sorting directions. CurdException is a custom exception. The entity class inheritance system manages common fields. The SQL monitoring module captures slow SQL and errors. The abstract JPA configuration class creates entity manager factories and data sources. MySpecification implements dynamic query condition construction. DataMysql is the base class for database operations. The Where class builds query conditions in a chainable manner. |

# Description

## Overview  
This module is a MySQL data access layer implemented around JPA, with its core responsibility being to provide standardized CRUD operations and dynamic query capabilities. The interface specification consists of three layers: the base repository interface (MyJpaRepository extending the native JPA interface), the condition builder (Where/MySpecification), and the pagination utility (PageUtils). Key data structures include the pagination object (Pageable), sorting enumeration (OrderBy), and condition items (Where.Item). External dependencies are limited to JPA and the Druid data source. For example, MyJpaRepository automatically handles pagination parameter validation through the getPageable method.

The module also implements SQL monitoring (similar to AOP aspects) and an entity base class inheritance hierarchy. SQL monitoring captures slow queries (threshold: 100ms) and erroneous SQL, recording statistical information via SlowSql/ErrorSql. The entity base classes (e.g., AbstractUniqueIDEntity) provide globally unique IDs (UUID) and timestamp management. For instance, AbstractBlockChainEntity extends log time fields to support blockchain scenarios.

## Main Business Scenarios  
The module is suitable for scenarios requiring dynamic queries and standardized data management, akin to an enhanced version of Spring Data JPA. A typical workflow involves: chaining conditions via Where (e.g., contains for fuzzy matching), generating dynamic Predicates with MySpecification, and executing paginated queries (e.g., getPageableForAtQuery) through MyJpaRepository. The interaction pattern uniformly combines conditions through method chaining, such as Where.equal().groupBy().build().

SQL monitoring implements end-to-end tracing via FilterEventAdapter, with business processes including: timing before execution, and updating statistics upon detecting slow queries/failures. The entity inheritance hierarchy supports rapid extension, such as blockchain entities inheriting from AbstractBlockChainEntity to automatically acquire log time fields. It fully covers closed-loop requirements from condition building (supporting 10+ operators) to paginated queries and monitoring analysis. For example, PageUtils uniformly handles single-object pagination, while CurdException encapsulates business exceptions.


### Package Internal Structure View

```mermaid
graph TD
    data --> mysql
    mysql --> repository
    mysql --> utils
    mysql --> enums
    mysql --> exception
    mysql --> entity
    mysql --> sql_monitor
    mysql --> config
    mysql --> MySpecification.java
    mysql --> DataMysql.java
    mysql --> Where.java
    repository --> MyJpaRepository.java
    utils --> PageUtils.java
    enums --> OrderBy.java
    exception --> CurdException.java
    entity --> AbstractUniqueIDEntity.java
    entity --> AbstractEntity.java
    entity --> AbstractBlockChainEntity.java
    sql_monitor --> SlowSql.java
    sql_monitor --> SqlMonitor.java
    sql_monitor --> ErrorSql.java
    config --> AbstractJpaConfig.java
```

This flowchart illustrates the complete hierarchical structure of the MySQL data module in the WeFe project. The root node "data" contains the main "mysql" module, which is further divided into 9 submodules and 3 independent files. Each submodule expands into specific implementation classes, such as the repository containing JPA repository implementations and the entity containing three types of abstract entity classes. The overall structure clearly reflects the modular design of the data access layer, encompassing core functionalities, utility classes, monitoring, and configuration as complete components.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [mysql](mysql/_module.md) | package | MyJpaRepository provides default methods for pagination queries and string processing. PageUtils handles pagination for single objects. The OrderBy enum defines sorting directions. CurdException serves as a custom exception. The entity class inheritance system manages common fields. The SQL monitoring module captures slow SQL and errors. The abstract JPA configuration class creates an entity manager factory and data source. MySpecification implements dynamic query condition construction. DataMysql serves as the base class for database operations. The Where class builds query conditions in a chainable manner. |


