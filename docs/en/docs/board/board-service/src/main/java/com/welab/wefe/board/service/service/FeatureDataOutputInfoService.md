# Basic Information

|      |      |
|------|------|
| Name | FeatureDataOutputInfoService |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/FeatureDataOutputInfoService.java |
| Package Name | com.welab.wefe.board.service.service |
| Dependencies | ['com.welab.wefe.board.service.database.entity.OutputModelMysqlModel', 'com.welab.wefe.board.service.database.entity.job.JobMySqlModel', 'com.welab.wefe.board.service.database.repository.JobRepository', 'com.welab.wefe.board.service.database.repository.OutputModelRepository', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| FeatureDataOutputInfoService | class |  |



## Class FeatureDataOutputInfoService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | FeatureDataOutputInfoService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| featureJobRepo | JobRepository |  |
| jobMemberService | JobMemberService |  |
| outputModelRepository | OutputModelRepository |  |
| taskService | TaskService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| wrapModelResult | JObject |  |
| find | JobMySqlModel |  |




