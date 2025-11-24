# Basic Information

|      |      |
|------|------|
| Name | HauckObliviousTransferSender |
| Language | .java |
| Code Path | WeFe/mpc/mpc-pir/mpc-pir-server/src/main/java/com/welab/wefe/mpc/pir/server/protocol/HauckObliviousTransferSender.java |
| Package Name | com.welab.wefe.mpc.pir.server.protocol |
| Dependencies | ['com.welab.wefe.mpc.commom.Conversion', 'com.welab.wefe.mpc.pir.protocol.nt.group.GroupElement', 'com.welab.wefe.mpc.pir.protocol.ot.ObliviousTransfer', 'com.welab.wefe.mpc.pir.protocol.ot.ObliviousTransferKey', 'com.welab.wefe.mpc.pir.protocol.ot.hauck.HauckObliviousTransfer', 'com.welab.wefe.mpc.pir.protocol.ot.hauck.HauckTarget', 'com.welab.wefe.mpc.pir.server.cache.HauckTargetCache', 'com.welab.wefe.mpc.pir.server.trasfer.PrivateInformationRetrievalTransferVariable', 'com.welab.wefe.mpc.pir.server.trasfer.impl.CacheTransferVariable', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.math.BigInteger', 'java.util.ArrayList', 'java.util.List', 'java.util.concurrent.CompletableFuture'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| HauckObliviousTransferSender | class |  |



## Class HauckObliviousTransferSender

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | HauckObliviousTransferSender |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| mTransferVariable = new CacheTransferVariable() | PrivateInformationRetrievalTransferVariable |  |
| LOG = LoggerFactory.getLogger(HauckObliviousTransferSender.class) | Logger |  |
| mHauckTarget = null | HauckTarget |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getHauckTarget | HauckTarget |  |
| keyDerivation | List<ObliviousTransferKey> |  |




