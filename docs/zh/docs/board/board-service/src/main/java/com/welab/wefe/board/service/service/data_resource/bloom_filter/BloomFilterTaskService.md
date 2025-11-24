# 基础信息

|      |      |
|------|------|
| 名称 | BloomFilterTaskService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/data_resource/bloom_filter/BloomFilterTaskService.java |
| 包名 | com.welab.wefe.board.service.service.data_resource.bloom_filter |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.fusion.bloomfilter.BloomFilterTaskMysqlModel', 'com.welab.wefe.board.service.database.repository.data_resource.BloomFilterRepository', 'com.welab.wefe.board.service.database.repository.fusion.BloomFilterTaskRepository', 'com.welab.wefe.board.service.service.AbstractService', 'com.welab.wefe.common.Convert', 'com.welab.wefe.common.data.mysql.Where', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.Date', 'java.util.function.Consumer'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| BloomFilterTaskService | class |  |



## 类 BloomFilterTaskService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | BloomFilterTaskService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| bloomfilterRepository | BloomFilterRepository |  |
| LOCKER = new Object() | Object |  |
| bloomfilterTaskRepository | BloomFilterTaskRepository |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| findById | BloomFilterTaskMysqlModel |  |
| onError | void |  |
| findByBloomfilterId | BloomFilterTaskMysqlModel |  |
| update | void |  |
| complete | void |  |
| updateProgress | void |  |




