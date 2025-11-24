# Basic Information

|      |      |
|------|------|
| Name | BloomFilterAddInputModel |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/vo/data_resource/BloomFilterAddInputModel.java |
| Package Name | com.welab.wefe.board.service.dto.vo.data_resource |
| Dependencies | ['com.welab.wefe.board.service.constant.BloomfilterAddMethod', 'com.welab.wefe.board.service.util.primarykey.FieldInfo', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'org.apache.commons.collections4.CollectionUtils', 'org.apache.commons.lang3.StringUtils', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BloomFilterAddInputModel | class |  |



## Class BloomFilterAddInputModel

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | BloomFilterAddInputModel |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| fieldInfoList | List<FieldInfo> |  |
| dataSourceId | String |  |
| deduplication | boolean |  |
| filename | String |  |
| hashFunction | String |  |
| sql | String |  |
| bloomfilterAddMethod | BloomfilterAddMethod |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getSql | String |  |
| setDataSourceId | void |  |
| getFieldInfoList | List<FieldInfo> |  |
| setFieldInfoList | void |  |
| setHashFunction | void |  |
| setBloomfilterAddMethod | void |  |
| getHashFunction | String |  |
| getDataSourceId | String |  |
| isDeduplication | boolean |  |
| getFilename | String |  |
| checkAndStandardize | void |  |
| setFilename | void |  |
| setSql | void |  |
| setDeduplication | void |  |
| getBloomfilterAddMethod | BloomfilterAddMethod |  |




