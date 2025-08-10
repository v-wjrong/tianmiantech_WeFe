# Basic Information

|      |      |
|------|------|
| Name | common-data-mongodb |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb |
| Package Name | docs.common.java.common-data-mongodb |
| Brief Description | The MongoDB data access layer provides CRUD and complex query capabilities, supporting logical deletion and timestamp constraints. It includes SMS business classification and vendor enumeration management. The toolkit supports chained query construction and aggregation operations. The federated learning platform implements logging, certificates, and data governance. Unified query management handles datasets and member authentication. The connection management module dynamically registers MongoDB components. |

# Description

## Overview  
This module serves as the core data management component of the federated learning platform, leveraging MongoDB to achieve unified storage and operations for multi-domain data, akin to a data bus pattern. Its core responsibilities include: 1) Managing 20+ business entities (e.g., certificates, datasets) through standardized CRUD interfaces; 2) Providing complex query construction tools and aggregation operation support; 3) Unified connection management and transaction control.  

The interface specification follows a layered design: the base layer (AbstractMongoModel/Repo) defines primary keys and serialization rules, while the business layer extends specific operations (e.g., version control). Key data structures include the pagination object PageOutput, certificate PEM content, and dataset permission models. External dependencies encompass Spring Data MongoDB, QueryBuilder, and MongoDB drivers. For instance, RealnameAuthAgreementTemplateMongoRepo implements optimistic lock updates, and QueryBuilder supports range filtering.  

## Key Business Scenarios  
The module supports four major scenarios: 1) Data governance (e.g., DataSet permission control), similar to the RBAC model; 2) Operation auditing (logging API call records); 3) Federated resource retrieval (multi-condition paginated queries); 4) Full lifecycle certificate management. Business processes include: selecting SMS templates via enumerations, chaining update conditions, and handling dataset permissions through aggregation pipelines.  

The interaction mode primarily involves DTO transfers and API compositions. For example, ImageDataSetMongoRepo combines label table queries, and AccountMongoRepo implements activity detection. Functional completeness is reflected in covering the entire data lifecycle (metadata → usage statistics), with typical applications including resource selectors during task configuration and node qualification validation. API types encompass CRUD operations (e.g., certStatus updates) and configuration classes (@Configuration). Integration examples can be observed in the block synchronization service's height records.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | The MongoDB data access layer provides CRUD and complex query capabilities, supporting logical deletion and timestamp constraints. It includes SMS business classification and vendor enumeration management. The toolkit supports chained query construction and aggregation operations. The federated learning platform implements logging, certificates, and data governance. Unified query management handles datasets and member authentication. The connection management module dynamically registers MongoDB components. |


