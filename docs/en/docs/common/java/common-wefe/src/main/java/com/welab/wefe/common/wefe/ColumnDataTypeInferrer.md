# Basic Information

|      |      |
|------|------|
| Name | ColumnDataTypeInferrer |
| Language | .java |
| Code Path | WeFe/common/java/common-wefe/src/main/java/com/welab/wefe/common/wefe/ColumnDataTypeInferrer.java |
| Package Name | com.welab.wefe.common.wefe |
| Dependencies | ['com.welab.wefe.common.CommonThreadPool', 'com.welab.wefe.common.Stopwatch', 'com.welab.wefe.common.Validator', 'com.welab.wefe.common.util.ThreadUtil', 'com.welab.wefe.common.wefe.enums.ColumnDataType', 'java.util', 'java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.atomic.LongAdder', 'java.util.function.Consumer'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ColumnDataTypeInferrer | class |  |



## Class ColumnDataTypeInferrer

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ColumnDataTypeInferrer |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| columnDataTypeInferCountMap = new ConcurrentHashMap<>() | Map<String, LongAdder> |  |
| counter = new LongAdder() | LongAdder |  |
| NULL_VALUE_LIST = Arrays.asList("", "null", "NA", "nan", "None") | List<String> |  |
| columns | List<String> |  |
| result = new LinkedHashMap<>() | LinkedHashMap<String, ColumnDataType> |  |
| columnDataTypes = new ConcurrentHashMap<>() | Map<String, Set<ColumnDataType>> |  |
| stopwatch = Stopwatch.startNew() | Stopwatch |  |
| samples = new ArrayList<>() | List<Map<String, Object>> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| inferDataType | ColumnDataType |  |
| inferRow | void |  |
| getColumnNames | List<String> |  |
| accept | void |  |
| getSamples | List<Map<String, Object>> |  |
| getResult | Map<String, ColumnDataType> |  |
| isEmptyValue | boolean |  |




