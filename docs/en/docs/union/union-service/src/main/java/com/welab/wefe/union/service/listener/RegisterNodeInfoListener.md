# Basic Information

|      |      |
|------|------|
| Name | RegisterNodeInfoListener |
| Language | .java |
| Code Path | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/listener/RegisterNodeInfoListener.java |
| Package Name | com.welab.wefe.union.service.listener |
| Dependencies | ['com.welab.wefe.common.data.mongodb.entity.union.UnionNode', 'com.welab.wefe.common.data.mongodb.entity.union.UnionNodeSm2Config', 'com.welab.wefe.common.data.mongodb.repo.UnionNodeConfigMongoRepo', 'com.welab.wefe.common.data.mongodb.repo.UnionNodeMongoRepo', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.SM2Util', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.union.service.cache.UnionNodeConfigCache', 'com.welab.wefe.union.service.constant.UnionNodeConfigType', 'com.welab.wefe.union.service.service.contract.UnionNodeContractService', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.beans.factory.annotation.Value', 'org.springframework.boot.context.event.ApplicationStartedEvent', 'org.springframework.context.ApplicationListener', 'org.springframework.stereotype.Component'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| RegisterNodeInfoListener | class |  |



## Class RegisterNodeInfoListener

|      |      |
|------|------|
| Access Modifier | @Component;public |
| Type | class |
| Name | RegisterNodeInfoListener |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| unionNodeMongoRepo | UnionNodeMongoRepo |  |
| currentBlockchainNodeId | String |  |
| unionNodeContractService | UnionNodeContractService |  |
| organizationName | String |  |
| LOG = LoggerFactory.getLogger(RegisterNodeInfoListener.class) | Logger |  |
| unionNodeConfigMongoRepo | UnionNodeConfigMongoRepo |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| onApplicationEvent | void |  |
| registerUnionNode | void |  |




