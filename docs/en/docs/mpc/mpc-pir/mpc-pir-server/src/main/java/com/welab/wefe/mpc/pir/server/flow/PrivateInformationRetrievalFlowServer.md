# Basic Information

|      |      |
|------|------|
| Name | PrivateInformationRetrievalFlowServer |
| Language | .java |
| Code Path | WeFe/mpc/mpc-pir/mpc-pir-server/src/main/java/com/welab/wefe/mpc/pir/server/flow/PrivateInformationRetrievalFlowServer.java |
| Package Name | com.welab.wefe.mpc.pir.server.flow |
| Dependencies | ['cn.hutool.core.util.ObjectUtil', 'com.alibaba.fastjson.JSON', 'com.welab.wefe.mpc.cache.intermediate.CacheOperation', 'com.welab.wefe.mpc.cache.intermediate.CacheOperationFactory', 'com.welab.wefe.mpc.commom.Constants', 'com.welab.wefe.mpc.commom.Conversion', 'com.welab.wefe.mpc.pir.flow.BasePrivateInformationRetrieval', 'com.welab.wefe.mpc.pir.protocol.ot.ObliviousTransferKey', 'com.welab.wefe.mpc.pir.protocol.se.SymmetricKey', 'com.welab.wefe.mpc.pir.protocol.se.aes.AESEncryptKey', 'com.welab.wefe.mpc.pir.server.protocol.HauckObliviousTransferSender', 'com.welab.wefe.mpc.pir.server.trasfer.PrivateInformationRetrievalTransferVariable', 'com.welab.wefe.mpc.pir.server.trasfer.impl.CacheTransferVariable', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.ArrayList', 'java.util.List', 'java.util.Map', 'java.util.concurrent.CompletableFuture', 'java.util.concurrent.TimeUnit'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PrivateInformationRetrievalFlowServer | class |  |



## Class PrivateInformationRetrievalFlowServer

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | PrivateInformationRetrievalFlowServer |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| mTransferVariable = new CacheTransferVariable() | PrivateInformationRetrievalTransferVariable |  |
| LOG = LoggerFactory.getLogger(PrivateInformationRetrievalFlowServer.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| initObliviousTransfer | void |  |
| process | void |  |
| setUuid | void |  |




