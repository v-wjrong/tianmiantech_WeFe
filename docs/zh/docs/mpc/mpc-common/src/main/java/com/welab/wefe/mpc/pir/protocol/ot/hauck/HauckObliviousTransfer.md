# 基础信息

|      |      |
|------|------|
| 名称 | HauckObliviousTransfer |
| 编码语言 | .java |
| 代码路径 | WeFe/mpc/mpc-common/src/main/java/com/welab/wefe/mpc/pir/protocol/ot/hauck/HauckObliviousTransfer.java |
| 包名 | com.welab.wefe.mpc.pir.protocol.ot.hauck |
| 依赖项 | ['com.welab.wefe.mpc.pir.protocol.nt.field.integers.IntegersModuloPrimeElement', 'com.welab.wefe.mpc.pir.protocol.nt.group.GroupArithmetic', 'com.welab.wefe.mpc.pir.protocol.nt.group.GroupElement', 'com.welab.wefe.mpc.pir.protocol.nt.group.cyclic.twisted.TwistedEdwardsCurveArithmetic', 'com.welab.wefe.mpc.pir.protocol.nt.group.cyclic.twisted.TwistedEdwardsCurveElement', 'com.welab.wefe.mpc.pir.protocol.ro.hf.HashFunction', 'com.welab.wefe.mpc.pir.protocol.ro.hf.Sha256', 'com.welab.wefe.mpc.pir.protocol.ro.mac.HashBasedMessageAuthenticationCode', 'com.welab.wefe.mpc.pir.protocol.ro.mac.Sha256MAC', 'java.math.BigInteger', 'java.security.SecureRandom'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| HauckObliviousTransfer | class |  |



## 类 HauckObliviousTransfer

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | HauckObliviousTransfer |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| mac | HashBasedMessageAuthenticationCode |  |
| uuid | String |  |
| arithmetic | GroupArithmetic |  |
| hash | HashFunction |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| generateHauckTarget | HauckTarget |  |
| genRandomScalar | BigInteger |  |
| hashTecElement | GroupElement |  |
| getGroupElement | GroupElement |  |
| macTecElement | byte[] |  |
| initMac | void |  |




