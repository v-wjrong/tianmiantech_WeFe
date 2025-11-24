# Basic Information

|      |      |
|------|------|
| Name | InitListener |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/listener/InitListener.java |
| Package Name | com.welab.wefe.gateway.listener |
| Dependencies | ['com.welab.wefe.gateway.cache.CaCertificateCache', 'com.welab.wefe.gateway.cache.PartnerConfigCache', 'com.welab.wefe.gateway.init', 'com.welab.wefe.gateway.init.grpc.GrpcServerContext', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.boot.context.event.ApplicationStartedEvent', 'org.springframework.context.ApplicationListener', 'org.springframework.stereotype.Component'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| InitListener | class |  |



## Class InitListener

|      |      |
|------|------|
| Access Modifier | @Component;public |
| Type | class |
| Name | InitListener |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(InitListener.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| onApplicationEvent | void |  |
| startGrpcServer | void |  |
| loadSystemConfigInfo | void |  |




