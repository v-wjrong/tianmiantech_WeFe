# 基础信息

|      |      |
|------|------|
| 名称 | BloomFilterAddInputModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/dto/vo/data_resource/BloomFilterAddInputModel.java |
| 包名 | com.welab.wefe.board.service.dto.vo.data_resource |
| 依赖项 | ['com.welab.wefe.board.service.constant.BloomfilterAddMethod', 'com.welab.wefe.board.service.util.primarykey.FieldInfo', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'org.apache.commons.collections4.CollectionUtils', 'org.apache.commons.lang3.StringUtils', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| BloomFilterAddInputModel | class |  |



## 类 BloomFilterAddInputModel

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | BloomFilterAddInputModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| fieldInfoList | List<FieldInfo> |  |
| dataSourceId | String |  |
| deduplication | boolean |  |
| filename | String |  |
| hashFunction | String |  |
| sql | String |  |
| bloomfilterAddMethod | BloomfilterAddMethod |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




