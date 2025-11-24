# Basic Information

|      |      |
|------|------|
| Name | BloomFilterTaskService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/data_resource/bloom_filter/BloomFilterTaskService.java |
| Package Name | com.welab.wefe.board.service.service.data_resource.bloom_filter |
| Dependencies | ['com.welab.wefe.board.service.database.entity.fusion.bloomfilter.BloomFilterTaskMysqlModel', 'com.welab.wefe.board.service.database.repository.data_resource.BloomFilterRepository', 'com.welab.wefe.board.service.database.repository.fusion.BloomFilterTaskRepository', 'com.welab.wefe.board.service.service.AbstractService', 'com.welab.wefe.common.Convert', 'com.welab.wefe.common.data.mysql.Where', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.Date', 'java.util.function.Consumer'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BloomFilterTaskService | class |  |



## Class BloomFilterTaskService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | BloomFilterTaskService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| bloomfilterRepository | BloomFilterRepository |  |
| LOCKER = new Object() | Object |  |
| bloomfilterTaskRepository | BloomFilterTaskRepository |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| findById | BloomFilterTaskMysqlModel |  |
| onError | void |  |
| findByBloomfilterId | BloomFilterTaskMysqlModel |  |
| update | void |  |
| complete | void |  |
| updateProgress | void |  |




