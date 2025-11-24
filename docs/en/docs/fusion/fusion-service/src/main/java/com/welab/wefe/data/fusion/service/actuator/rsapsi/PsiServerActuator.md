# Basic Information

|      |      |
|------|------|
| Name | PsiServerActuator |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/actuator/rsapsi/PsiServerActuator.java |
| Package Name | com.welab.wefe.data.fusion.service.actuator.rsapsi |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.CommonThreadPool', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.data.fusion.service.enums.ActionType', 'com.welab.wefe.data.fusion.service.enums.PSIActuatorStatus', 'com.welab.wefe.data.fusion.service.utils.FusionUtils', 'com.welab.wefe.data.fusion.service.utils.bf.BloomFilters', 'com.welab.wefe.fusion.core.utils.CryptoUtils', 'com.welab.wefe.fusion.core.utils.PSIUtils', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.DataOutputStream', 'java.io.IOException', 'java.math.BigInteger', 'java.net.InetAddress', 'java.net.ServerSocket', 'java.net.Socket', 'java.util.ArrayList', 'java.util.HashMap', 'java.util.List', 'java.util.Map'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PsiServerActuator | class |  |



## Class PsiServerActuator

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | PsiServerActuator |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| threadId = new ThreadLocal<>() | ThreadLocal<Integer> |  |
| e | BigInteger |  |
| cacheMap = new HashMap<>() | Map<Integer, byte[][]> |  |
| d | BigInteger |  |
| serverSocket | ServerSocket |  |
| N | BigInteger |  |
| LOG = LoggerFactory.getLogger(PsiServerActuator.class) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| end | void |  |
| sendBloomFilter | void |  |
| start | void |  |
| receiveResult | void |  |
| align | void |  |
| fillBloomFilters | PsiServerActuator |  |
| listen | void |  |
| execute | void |  |
| close | void |  |
| init | void |  |
| handle | void |  |




