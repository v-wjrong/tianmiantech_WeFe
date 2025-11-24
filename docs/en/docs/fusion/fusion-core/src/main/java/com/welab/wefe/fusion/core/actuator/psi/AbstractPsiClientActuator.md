# Basic Information

|      |      |
|------|------|
| Name | AbstractPsiClientActuator |
| Language | .java |
| Code Path | WeFe/fusion/fusion-core/src/main/java/com/welab/wefe/fusion/core/actuator/psi/AbstractPsiClientActuator.java |
| Package Name | com.welab.wefe.fusion.core.actuator.psi |
| Dependencies | ['java.math.BigInteger', 'java.security.SecureRandom', 'java.util.ArrayList', 'java.util.List', 'java.util.concurrent.ExecutorService', 'java.util.concurrent.Executors', 'java.util.concurrent.TimeUnit', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.ThreadUtil', 'com.welab.wefe.fusion.core.dto.PsiActuatorMeta', 'com.welab.wefe.fusion.core.enums.PSIActuatorStatus', 'com.welab.wefe.fusion.core.utils.PSIUtils'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractPsiClientActuator | class |  |



## Class AbstractPsiClientActuator

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractPsiClientActuator |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| isTrace | Boolean |  |
| psiClientMeta | PsiActuatorMeta |  |
| dataSetId | String |  |
| traceColumn | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| generateBlindingFactor | BigInteger |  |
| fusion | void |  |
| getRandom | BigInteger |  |
| parseAndMatch | List<JObject> |  |
| execute | void |  |




