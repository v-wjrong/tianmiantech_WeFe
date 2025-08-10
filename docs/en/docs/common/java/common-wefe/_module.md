# Basic Information

|      |      |
|------|------|
| Name | common-wefe |
| Language | .java |
| Code Path | WeFe/common/java/common-wefe |
| Package Name | docs.common.java.common-wefe |
| Brief Description | The service inspection framework implements hierarchical health checks, the enumeration module defines federated learning type states, the configuration management module uniformly handles multi-source connections, and the data type inferrer analyzes field types. |

# Description

## Overview  
This module serves as the core supporting framework for federated learning systems, encompassing four major functionalities: service health check, enumeration definitions, configuration management, and data type inference. It adopts a layered abstraction design, with key interfaces including AbstractCheckpoint (checkpoint), AbstractConfigModel (configuration model), and Consumer (data type inference). Core data structures cover ServiceCheckPointOutput (inspection results), 11 types of ServiceType (service type enumerations), and ColumnDataType (field type). It relies on the Spring framework, JDBC drivers, and cloud service SDKs. For example, CheckpointManager concurrently tests UnionService connectivity, or ColumnDataTypeInferrer deduces field types.

## Key Business Scenarios  
The module supports full lifecycle management of federated learning: 1) Service health check adopts a sentinel pattern, such as 5-second timeout detection; 2) Enumeration-driven state machines, e.g., JobStatus controls task flow; 3) Factory pattern manages multi-data source configurations, such as generating specialized database URLs; 4) Multi-threaded field type inference (similar to MapReduce). Typical workflows include configuration validation → parallel checks → result aggregation, e.g., escalating UnionService check failures level by level. Integration cases span horizontal federated learning (using XGBoost algorithms) and cloud storage switching (e.g., OSS credential management).


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | The service inspection framework implements hierarchical health checks, the enumeration module defines federated learning type states, the configuration management module uniformly handles multi-source connections, and the data type inferrer analyzes field types. |


