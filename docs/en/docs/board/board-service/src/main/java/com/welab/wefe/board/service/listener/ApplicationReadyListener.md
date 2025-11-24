# Basic Information

|      |      |
|------|------|
| Name | ApplicationReadyListener |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/listener/ApplicationReadyListener.java |
| Package Name | com.welab.wefe.board.service.listener |
| Dependencies | ['com.welab.wefe.board.service.database.repository.data_resource.DataResourceUploadTaskRepository', 'com.welab.wefe.board.service.service.globalconfig.GlobalConfigService', 'com.welab.wefe.common.util.HostUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.wefe.dto.global_config.GatewayConfigModel', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.boot.context.event.ApplicationReadyEvent', 'org.springframework.context.ApplicationListener', 'org.springframework.stereotype.Component'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ApplicationReadyListener | class |  |



## Class ApplicationReadyListener

|      |      |
|------|------|
| Access Modifier | @Component;public |
| Type | class |
| Name | ApplicationReadyListener |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| globalConfigService | GlobalConfigService |  |
| dataResourceUploadTaskRepository | DataResourceUploadTaskRepository |  |
| LOG = LoggerFactory.getLogger(ApplicationReadyListener.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| appendIpAddressToGatewayWhiteList | void |  |
| onApplicationEvent | void |  |




