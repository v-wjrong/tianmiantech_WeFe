# Basic Information

|      |      |
|------|------|
| Name | common-jdbc |
| Language | .java |
| Code Path | WeFe/common/java/common-jdbc |
| Package Name | docs.common.java.common-jdbc |
| Brief Description | HiveScanner and MysqlScanner are subclasses of JdbcScanner, designed for Hive and MySQL queries respectively. JdbcScanner is an abstract base class that encapsulates the JDBC query process and supports multi-database adaptation. JdbcClient encapsulates JDBC operations, supports various databases, and provides connection management, batch writing, and streaming query functionalities. |

# Description

## Overview  
The core responsibility of this module is to provide a unified JDBC operation framework for multiple databases, including type identification, connection management, and data scanning functionality. The `DatabaseType` enum defines six database types, while `JdbcScanner` serves as an abstract base class implementing a query process similar to a result set iterator. `JdbcClient` encapsulates complete JDBC operations. Key data structures include the `DatabaseType` enum, scanner classes containing `Connection`/`ResultSet`, and `JdbcClient` configuration parameters. The only external dependency is the standard JDBC interface. For example, `HiveScanner` optimizes queries through prepared statements, and `MysqlScanner` sets a special fetch size to improve performance.  

## Primary Business Scenarios  
This module is suitable for batch data operations across databases, such as multi-source data synchronization in ETL tools. A typical workflow involves: establishing a connection via `JdbcClient`, using `JdbcScanner` to execute streaming queries to avoid memory overflow, or performing batch writes to enhance efficiency. For instance, when reading tens of millions of rows from Hive, pagination can be controlled via `maxRows`. The interaction model supports the standard "connect-query-iterate-close" workflow and prepared statement optimization, offering features like table structure retrieval and field projection. The API includes a factory pattern for creating `JdbcClient`, a template method pattern for implementing scanner subclasses (e.g., `MysqlScanner`), and a `Closeable` resource management interface.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | HiveScanner and MysqlScanner are subclasses of JdbcScanner, designed for Hive and MySQL queries respectively. JdbcScanner is an abstract base class that encapsulates the JDBC query process and supports multi-database adaptation. JdbcClient encapsulates JDBC operations, supports various databases, and provides connection management, batch writing, and streaming query functionalities. |


