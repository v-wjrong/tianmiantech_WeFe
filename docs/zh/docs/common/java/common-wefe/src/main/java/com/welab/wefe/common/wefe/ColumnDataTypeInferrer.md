# 基础信息

|      |      |
|------|------|
| 名称 | ColumnDataTypeInferrer |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-wefe/src/main/java/com/welab/wefe/common/wefe/ColumnDataTypeInferrer.java |
| 包名 | com.welab.wefe.common.wefe |
| 依赖项 | ['com.welab.wefe.common.CommonThreadPool', 'com.welab.wefe.common.Stopwatch', 'com.welab.wefe.common.Validator', 'com.welab.wefe.common.util.ThreadUtil', 'com.welab.wefe.common.wefe.enums.ColumnDataType', 'java.util', 'java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.atomic.LongAdder', 'java.util.function.Consumer'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ColumnDataTypeInferrer | class |  |



## 类 ColumnDataTypeInferrer

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ColumnDataTypeInferrer |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| columnDataTypeInferCountMap = new ConcurrentHashMap<>() | Map<String, LongAdder> |  |
| counter = new LongAdder() | LongAdder |  |
| NULL_VALUE_LIST = Arrays.asList("", "null", "NA", "nan", "None") | List<String> |  |
| columns | List<String> |  |
| result = new LinkedHashMap<>() | LinkedHashMap<String, ColumnDataType> |  |
| columnDataTypes = new ConcurrentHashMap<>() | Map<String, Set<ColumnDataType>> |  |
| stopwatch = Stopwatch.startNew() | Stopwatch |  |
| samples = new ArrayList<>() | List<Map<String, Object>> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| inferDataType | ColumnDataType |  |
| inferRow | void |  |
| getColumnNames | List<String> |  |
| accept | void |  |
| getSamples | List<Map<String, Object>> |  |
| getResult | Map<String, ColumnDataType> |  |
| isEmptyValue | boolean |  |




