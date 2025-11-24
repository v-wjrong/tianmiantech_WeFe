# Basic Information

|      |      |
|------|------|
| Name | HauckObliviousTransferReceiver |
| Language | .java |
| Code Path | WeFe/mpc/mpc-pir/mpc-pir-sdk/src/main/java/com/welab/wefe/mpc/pir/sdk/protocol/HauckObliviousTransferReceiver.java |
| Package Name | com.welab.wefe.mpc.pir.sdk.protocol |
| Dependencies | ['java.math.BigInteger', 'java.util.ArrayList', 'java.util.List', 'java.util.concurrent.CompletableFuture', 'java.util.concurrent.ExecutionException', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.welab.wefe.mpc.commom.Conversion', 'com.welab.wefe.mpc.pir.protocol.nt.group.GroupArithmetic', 'com.welab.wefe.mpc.pir.protocol.nt.group.GroupElement', 'com.welab.wefe.mpc.pir.protocol.ot.ObliviousTransfer', 'com.welab.wefe.mpc.pir.protocol.ot.ObliviousTransferKey', 'com.welab.wefe.mpc.pir.protocol.ot.hauck.HauckObliviousTransfer', 'com.welab.wefe.mpc.pir.request.QueryRandomLegalRequest', 'com.welab.wefe.mpc.pir.request.QueryRandomLegalResponse', 'com.welab.wefe.mpc.pir.request.QueryRandomRequest', 'com.welab.wefe.mpc.pir.sdk.trasfer.PrivateInformationRetrievalTransferVariable', 'com.welab.wefe.mpc.util.EncryptUtil', 'cn.hutool.core.util.StrUtil'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| HauckObliviousTransferReceiver | class |  |



## Class HauckObliviousTransferReceiver

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | HauckObliviousTransferReceiver |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(HauckObliviousTransferReceiver.class) | Logger |  |
| mTransferVariable | PrivateInformationRetrievalTransferVariable |  |
| firstS | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| sendR | QueryRandomLegalResponse |  |
| keyDerivation | List<ObliviousTransferKey> |  |
| calcR | GroupElement |  |
| checkSLegal | boolean |  |




