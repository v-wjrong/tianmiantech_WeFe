# Basic Information

|      |      |
|------|------|
| Name | QueryBuilder |
| Language | .java |
| Code Path | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/util/QueryBuilder.java |
| Package Name | com.welab.wefe.common.data.mongodb.util |
| Dependencies | ['org.apache.commons.lang3.StringUtils', 'org.springframework.data.domain.Sort', 'org.springframework.data.mongodb.core.query.Criteria', 'org.springframework.data.mongodb.core.query.Query', 'java.util'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| QueryBuilder | class |  |



## Class QueryBuilder

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | QueryBuilder |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| pageIndex | Integer |  |
| sortMap = new LinkedHashMap<>() | Map<String, Boolean> |  |
| eqMap = new LinkedHashMap<>() | Map<String, Object> |  |
| timeBetween = new long[2] | long[] |  |
| dateBetweenMap = new LinkedHashMap<>() | Map<String, Date[]> |  |
| likeMap = new LinkedHashMap<>() | Map<String, String> |  |
| inMap = new LinkedHashMap<>() | Map<String, List<?>> |  |
| timeWithin | long |  |
| lteMap = new LinkedHashMap<>() | Map<String, Object> |  |
| noteqMap = new LinkedHashMap<>() | Map<String, Object> |  |
| existMap = new LinkedHashMap<>() | Map<String, Boolean> |  |
| pageSize | Integer |  |
| gteMap = new LinkedHashMap<>() | Map<String, Object> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| sort | QueryBuilder |  |
| betweenByDate | QueryBuilder |  |
| in | QueryBuilder |  |
| withinDays | QueryBuilder |  |
| append | QueryBuilder |  |
| withinMinutes | QueryBuilder |  |
| notRemoved | QueryBuilder |  |
| gte | QueryBuilder |  |
| notEq | QueryBuilder |  |
| between | QueryBuilder |  |
| page | QueryBuilder |  |
| sort | QueryBuilder |  |
| exist | QueryBuilder |  |
| lte | QueryBuilder |  |
| like | QueryBuilder |  |
| getCriteria | Criteria |  |
| build | Query |  |
| escapeExprSpecialWord | String |  |




