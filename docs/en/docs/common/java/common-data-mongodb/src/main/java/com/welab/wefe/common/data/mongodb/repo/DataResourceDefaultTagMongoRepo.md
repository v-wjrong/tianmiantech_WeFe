# Basic Information

|      |      |
|------|------|
| Name | DataResourceDefaultTagMongoRepo |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/repo/DataResourceDefaultTagMongoRepo.java |
| Package Name | com.welab.wefe.common.data.mongodb.repo |
| Dependencies | ['com.mongodb.client.result.UpdateResult', 'com.welab.wefe.common.data.mongodb.entity.union.DataResourceDefaultTag', 'com.welab.wefe.common.data.mongodb.entity.union.ext.DataResourceDefaultTagExtJSON', 'com.welab.wefe.common.data.mongodb.util.QueryBuilder', 'com.welab.wefe.common.data.mongodb.util.UpdateBuilder', 'org.apache.commons.lang3.StringUtils', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.mongodb.core.MongoTemplate', 'org.springframework.data.mongodb.core.query.Query', 'org.springframework.data.mongodb.core.query.Update', 'org.springframework.stereotype.Repository', 'java.util.List'] |
| Brief Description | The `DataResourceDefaultTagMongoRepo` class inherits from `AbstractMongoRepo` and utilizes `MongoTemplate` to interact with MongoDB. It provides methods such as `exists`, `findByDataResourceType`, `deleteByTagId`, `update`, and `updateExtJSONById` for querying, deleting, and updating `DataResourceDefaultTag` data. |

# Description

This is a MongoDB data access class named DataResourceDefaultTagMongoRepo, which inherits from AbstractMongoRepo. It utilizes MongoTemplate for database operations, with primary functionalities including: checking if a tag name exists, querying tags by resource type, deleting tags (logical deletion), updating tag information (name, extended JSON, and update time), and separately updating the extended JSON of a tag. All operations include non-null validation and are performed on the DataResourceDefaultTag class.

# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataResourceDefaultTagMongoRepo | class | The DataResourceDefaultTagMongoRepo class inherits from AbstractMongoRepo, providing functionalities such as tag existence checks, querying by type, deletion, updates, and extended JSON updates, utilizing MongoTemplate for database operations. |



## Class DataResourceDefaultTagMongoRepo

|      |      |
|------|------|
| Access Modifier | @Repository;public |
| Type | class |
| Name | DataResourceDefaultTagMongoRepo |
| Description | The DataResourceDefaultTagMongoRepo class inherits from AbstractMongoRepo, providing functionalities such as tag existence checks, querying by type, deletion, updates, and extended JSON updates, utilizing MongoTemplate for database operations. |


### UML Class Diagram

```mermaid
classDiagram
    class AbstractMongoRepo {
        <<Abstract>>
        #MongoTemplate getMongoTemplate()*
    }

    class DataResourceDefaultTagMongoRepo {
        <<Repository>>
        -MongoTemplate mongoUnionTemplate
        +boolean exists(String tagName)
        +List~DataResourceDefaultTag~ findByDataResourceType(String dataResourceType)
        +boolean deleteByTagId(String tagId)
        +boolean update(String tagId, String tagName, DataResourceDefaultTagExtJSON extJson, String updatedTime)
        +boolean updateExtJSONById(String tagId, DataResourceDefaultTagExtJSON extJSON)
        #MongoTemplate getMongoTemplate()
    }

    class DataResourceDefaultTag {
        // Data resource default tag entity class
    }

    class DataResourceDefaultTagExtJSON {
        // Tag extension JSON data class
    }

    class QueryBuilder {
        +QueryBuilder append(String key, Object value)
        +QueryBuilder notRemoved()
        +Query build()
    }

    class UpdateBuilder {
        +UpdateBuilder append(String key, Object value)
        +Update build()
    }

    AbstractMongoRepo <|-- DataResourceDefaultTagMongoRepo
    DataResourceDefaultTagMongoRepo --> DataResourceDefaultTag : Operates
    DataResourceDefaultTagMongoRepo --> DataResourceDefaultTagExtJSON : Contains
    DataResourceDefaultTagMongoRepo --> QueryBuilder : Builds queries
    DataResourceDefaultTagMongoRepo --> UpdateBuilder : Builds updates
    DataResourceDefaultTagMongoRepo --> MongoTemplate : Depends on
```

This code demonstrates a MongoDB repository class `DataResourceDefaultTagMongoRepo`, which inherits from the abstract class `AbstractMongoRepo` and is primarily used for CRUD operations on the `DataResourceDefaultTag` entity. The class constructs query and update conditions using `QueryBuilder` and `UpdateBuilder`, and executes database operations via `MongoTemplate`. Key functionalities include checking tag existence, finding tags by resource type, deleting/updating tags, etc., with all methods incorporating parameter validation and status checks.


### Internal Method Call Graph

```mermaid
graph TD
    A["Class DataResourceDefaultTagMongoRepo"]
    B["Property: MongoTemplate mongoUnionTemplate"]
    C["Method: MongoTemplate getMongoTemplate()"]
    D["Method: boolean exists(String tagName)"]
    E["Method: List<DataResourceDefaultTag> findByDataResourceType(String dataResourceType)"]
    F["Method: boolean deleteByTagId(String tagId)"]
    G["Method: boolean update(String tagId, String tagName, DataResourceDefaultTagExtJSON extJson, String updatedTime)"]
    H["Method: boolean updateExtJSONById(String tagId, DataResourceDefaultTagExtJSON extJSON)"]

    A --> B
    A --> C
    A --> D
    A --> E
    A --> F
    A --> G
    A --> H

    D --> D1["Create Query: QueryBuilder.append('tagName', tagName).notRemoved().build()"]
    D1 --> D2["Call mongoUnionTemplate.exists()"]
    E --> E1["Create Query: QueryBuilder.notRemoved().append('dataResourceType', dataResourceType).build()"]
    E1 --> E2["Call mongoUnionTemplate.find()"]
    F --> F1["Check tagId null"]
    F1 -->|Not null| F2["Create Query: QueryBuilder.append('tagId', tagId).build()"]
    F2 --> F3["Create Update: UpdateBuilder.append('status', 1).build()"]
    F3 --> F4["Call mongoUnionTemplate.updateFirst()"]
    G --> G1["Check tagId null"]
    G1 -->|Not null| G2["Create Query: QueryBuilder.append('tagId', tagId).build()"]
    G2 --> G3["Create Update: UpdateBuilder.append('tagName', tagName).append('extJson', extJson).append('updatedTime', updatedTime).build()"]
    G3 --> G4["Call mongoUnionTemplate.updateFirst()"]
    H --> H1["Check tagId null"]
    H1 -->|Not null| H2["Create Query: QueryBuilder.append('tagId', tagId).build()"]
    H2 --> H3["Create Update: UpdateBuilder.append('extJson', extJSON).build()"]
    H3 --> H4["Call mongoUnionTemplate.updateFirst()"]
```

This flowchart illustrates the complete structure of the DataResourceDefaultTagMongoRepo class, featuring 5 core methods: exists() for tag existence verification, findByDataResourceType() for tag query by type, deleteByTagId() for soft tag deletion, update() for full-field tag updates, and updateExtJSONById() for partial JSON extension updates. All database operations are executed via mongoUnionTemplate, with key steps including Query construction, null checks, and Update operations, demonstrating atomic MongoDB operation encapsulation.

### Field List

| Name  | Type  | Description |
|-------|-------|------|
| mongoUnionTemplate | MongoTemplate | Use @Autowired to automatically inject the MongoTemplate instance mongoUnionTemplate. |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| findByDataResourceType | List<DataResourceDefaultTag> | This method queries MongoDB for undeleted DataResourceDefaultTag data matching the specified type and returns a result list. |
| getMongoTemplate | MongoTemplate | Rewrite the getMongoTemplate method to return a mongoUnionTemplate instance. |
| deleteByTagId | boolean | This method deletes data by tag ID, first verifying the ID's validity, then constructing query and update conditions, and finally executing the MongoDB update operation and returning whether it was successful. |
| exists | boolean | Check if the specified tag name exists, query undeleted tags and return the result. |
| update | boolean | This method updates the tag information in MongoDB based on the tagId, including the tagName, extJson, and updatedTime fields. If the tagId is empty, it returns false; otherwise, it performs the update and returns whether the operation was successful. |
| updateExtJSONById | boolean | The method updates the extJSON field in MongoDB by tagId, first validating that tagId is not empty, then constructing the query and update conditions, executing the update operation, and returning whether it was successful. |




