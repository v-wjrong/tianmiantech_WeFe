# Basic Information

|      |      |
|------|------|
| Name | FileSystemCheckpoint |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/service/processors/available/checkpoint/FileSystemCheckpoint.java |
| Package Name | com.welab.wefe.gateway.service.processors.available.checkpoint |
| Dependencies | ['com.welab.wefe.common.util.FileUtil', 'com.welab.wefe.common.wefe.checkpoint.AbstractCheckpoint', 'com.welab.wefe.common.wefe.enums.ServiceType', 'com.welab.wefe.gateway.config.ConfigProperties', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.stereotype.Service', 'java.io.File', 'java.nio.file.Path', 'java.nio.file.Paths'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| FileSystemCheckpoint | class |  |



## Class FileSystemCheckpoint

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | FileSystemCheckpoint |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| mConfigProperties | ConfigProperties |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| service | ServiceType |  |
| messageWhenConfigValueEmpty | String |  |
| getConfigValue | String |  |
| desc | String |  |
| doCheck | void |  |
| testCreateDir | void |  |




