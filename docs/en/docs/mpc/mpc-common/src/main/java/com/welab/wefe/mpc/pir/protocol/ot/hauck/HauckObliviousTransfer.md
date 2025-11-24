# Basic Information

|      |      |
|------|------|
| Name | HauckObliviousTransfer |
| Language | .java |
| Code Path | WeFe/mpc/mpc-common/src/main/java/com/welab/wefe/mpc/pir/protocol/ot/hauck/HauckObliviousTransfer.java |
| Package Name | com.welab.wefe.mpc.pir.protocol.ot.hauck |
| Dependencies | ['com.welab.wefe.mpc.pir.protocol.nt.field.integers.IntegersModuloPrimeElement', 'com.welab.wefe.mpc.pir.protocol.nt.group.GroupArithmetic', 'com.welab.wefe.mpc.pir.protocol.nt.group.GroupElement', 'com.welab.wefe.mpc.pir.protocol.nt.group.cyclic.twisted.TwistedEdwardsCurveArithmetic', 'com.welab.wefe.mpc.pir.protocol.nt.group.cyclic.twisted.TwistedEdwardsCurveElement', 'com.welab.wefe.mpc.pir.protocol.ro.hf.HashFunction', 'com.welab.wefe.mpc.pir.protocol.ro.hf.Sha256', 'com.welab.wefe.mpc.pir.protocol.ro.mac.HashBasedMessageAuthenticationCode', 'com.welab.wefe.mpc.pir.protocol.ro.mac.Sha256MAC', 'java.math.BigInteger', 'java.security.SecureRandom'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| HauckObliviousTransfer | class |  |



## Class HauckObliviousTransfer

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | HauckObliviousTransfer |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| mac | HashBasedMessageAuthenticationCode |  |
| uuid | String |  |
| arithmetic | GroupArithmetic |  |
| hash | HashFunction |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| generateHauckTarget | HauckTarget |  |
| genRandomScalar | BigInteger |  |
| hashTecElement | GroupElement |  |
| getGroupElement | GroupElement |  |
| macTecElement | byte[] |  |
| initMac | void |  |




