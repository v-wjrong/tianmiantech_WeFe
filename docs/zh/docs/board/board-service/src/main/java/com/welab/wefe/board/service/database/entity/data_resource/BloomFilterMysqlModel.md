# 基础信息

|      |      |
|------|------|
| 名称 | BloomFilterMysqlModel |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/database/entity/data_resource/BloomFilterMysqlModel.java |
| 包名 | com.welab.wefe.board.service.database.entity.data_resource |
| 依赖项 | ['com.welab.wefe.board.service.constant.BloomfilterAddMethod', 'com.welab.wefe.common.wefe.enums.DataResourceType', 'javax.persistence'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| BloomFilterMysqlModel | class |  |



## 类 BloomFilterMysqlModel

|      |      |
|------|------|
| 访问范围 | @Entity(name = "bloom_filter");@Table(name = "bloom_filter");public |
| 类型 | class |
| 名称 | BloomFilterMysqlModel |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| sqlScript | String |  |
| rsaN | String |  |
| addMethod | BloomfilterAddMethod |  |
| sourcePath | String |  |
| dataSourceId | String |  |
| rsaP | String |  |
| rsaE | String |  |
| rsaD | String |  |
| rsaQ | String |  |
| hashFunction | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| setSourcePath | void |  |
| getSourcePath | String |  |
| getRsaP | String |  |
| setSqlScript | void |  |
| getRsaN | String |  |
| setAddMethod | void |  |
| setRsaN | void |  |
| getSqlScript | String |  |
| getDataSourceId | String |  |
| setHashFunction | void |  |
| getHashFunction | String |  |
| setRsaD | void |  |
| getRsaD | String |  |
| setRsaE | void |  |
| getRsaE | String |  |
| getAddMethod | BloomfilterAddMethod |  |
| setDataSourceId | void |  |
| setRsaP | void |  |
| getRsaQ | String |  |
| setRsaQ | void |  |




