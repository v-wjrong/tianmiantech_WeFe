# 基础信息

|      |      |
|------|------|
| 名称 | FeatureDataOutputInfoService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/FeatureDataOutputInfoService.java |
| 包名 | com.welab.wefe.board.service.service |
| 依赖项 | ['com.welab.wefe.board.service.database.entity.OutputModelMysqlModel', 'com.welab.wefe.board.service.database.entity.job.JobMySqlModel', 'com.welab.wefe.board.service.database.repository.JobRepository', 'com.welab.wefe.board.service.database.repository.OutputModelRepository', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.wefe.enums.JobMemberRole', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| FeatureDataOutputInfoService | class |  |



## 类 FeatureDataOutputInfoService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | FeatureDataOutputInfoService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| featureJobRepo | JobRepository |  |
| jobMemberService | JobMemberService |  |
| outputModelRepository | OutputModelRepository |  |
| taskService | TaskService |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| wrapModelResult | JObject |  |
| find | JobMySqlModel |  |




