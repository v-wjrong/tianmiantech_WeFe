# 基础信息

|      |      |
|------|------|
| 名称 | QueryBuilder |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mongodb/src/main/java/com/welab/wefe/common/data/mongodb/util/QueryBuilder.java |
| 包名 | com.welab.wefe.common.data.mongodb.util |
| 依赖项 | ['org.apache.commons.lang3.StringUtils', 'org.springframework.data.domain.Sort', 'org.springframework.data.mongodb.core.query.Criteria', 'org.springframework.data.mongodb.core.query.Query', 'java.util'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| QueryBuilder | class |  |



## 类 QueryBuilder

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | QueryBuilder |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




