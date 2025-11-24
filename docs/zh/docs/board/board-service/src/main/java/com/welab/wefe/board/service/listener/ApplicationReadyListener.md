# 基础信息

|      |      |
|------|------|
| 名称 | ApplicationReadyListener |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/listener/ApplicationReadyListener.java |
| 包名 | com.welab.wefe.board.service.listener |
| 依赖项 | ['com.welab.wefe.board.service.database.repository.data_resource.DataResourceUploadTaskRepository', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.util.HostUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.dto.global_config.GatewayConfigModel', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.boot.context.event.ApplicationReadyEvent', 'org.springframework.context.ApplicationListener', 'org.springframework.stereotype.Component'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ApplicationReadyListener | class |  |



## 类 ApplicationReadyListener

|      |      |
|------|------|
| 访问范围 | @Component;public |
| 类型 | class |
| 名称 | ApplicationReadyListener |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| globalConfigService | GlobalConfigService |  |
| dataResourceUploadTaskRepository | DataResourceUploadTaskRepository |  |
| LOG = LoggerFactory.getLogger(ApplicationReadyListener.class) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| appendIpAddressToGatewayWhiteList | void |  |
| onApplicationEvent | void |  |




