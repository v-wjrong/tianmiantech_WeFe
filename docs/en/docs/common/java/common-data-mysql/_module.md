# Basic Information

|      |      |
|------|------|
| Name | common-data-mysql |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mysql |
| Package Name | docs.common.java.common-data-mysql |
| Brief Description | MyJpaRepository provides default methods for pagination queries and string processing. PageUtils handles pagination for single objects. The OrderBy enum defines sorting directions. CurdException is a custom exception. The entity class inheritance hierarchy manages common fields. The SQL monitoring module captures slow SQL and errors. The abstract JPA configuration class creates the entity manager factory and data source. MySpecification implements dynamic query condition construction. DataMysql is the base class for database operations. The Where class builds query conditions in a chainable manner. |

# Description

## Overview  
This module is a MySQL data access layer implemented around JPA, with its core responsibility being to provide standardized CRUD operations and dynamic query capabilities. The interface specification consists of three layers: the base repository interface (MyJpaRepository extending native JPA interfaces), the condition builder (Where/MySpecification), and the pagination utility (PageUtils). Key data structures include the pagination object (Pageable), sorting enumeration (OrderBy), and condition items (Where.Item). External dependencies are limited to JPA and the Druid data source. For example, MyJpaRepository automatically handles pagination parameter validation through the getPageable method.  

The module also implements SQL monitoring (similar to AOP aspects) and an entity base class inheritance hierarchy. SQL monitoring captures slow queries (threshold: 100ms) and erroneous SQL, recording statistical information via SlowSql/ErrorSql. Entity base classes (e.g., AbstractUniqueIDEntity) provide globally unique IDs (UUID) and timestamp management. For instance, AbstractBlockChainEntity extends log time fields to support blockchain scenarios.  

## Key Business Scenarios  
The module is suitable for scenarios requiring dynamic queries and standardized data management, akin to an enhanced version of Spring Data JPA. A typical workflow involves: chaining conditions via Where (e.g., contains for fuzzy matching), generating dynamic Predicates with MySpecification, and executing paginated queries (e.g., getPageableForAtQuery) through MyJpaRepository. The interaction pattern uniformly combines conditions via method chaining, such as Where.equal().groupBy().build().  

SQL monitoring implements end-to-end tracing through FilterEventAdapter, with business processes including: timing before execution, and updating statistics upon detecting slow queries/failures. The entity inheritance hierarchy supports rapid extension, such as blockchain entities inheriting AbstractBlockChainEntity to automatically acquire log time fields. It fully covers closed-loop requirements from condition building (supporting 10+ operators) to paginated queries and monitoring analysis. For example, PageUtils standardizes pagination for single objects, while CurdException encapsulates business exceptions.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | MyJpaRepository provides default methods for pagination queries and string processing. PageUtils handles pagination for single objects. The OrderBy enum defines sorting directions. CurdException is a custom exception. The entity class inheritance system manages common fields. The SQL monitoring module captures slow SQL and errors. The abstract JPA configuration class creates entity manager factories and data sources. MySpecification implements dynamic query condition construction. DataMysql is the base class for database operations. The Where class builds query conditions in a chainable manner. |


