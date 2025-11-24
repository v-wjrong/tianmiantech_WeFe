# 基础信息

|      |      |
|------|------|
| 名称 | PsiServerActuator |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/actuator/rsapsi/PsiServerActuator.java |
| 包名 | com.welab.wefe.data.fusion.service.actuator.rsapsi |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.CommonThreadPool', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.data.fusion.service.enums.ActionType', 'com.welab.wefe.data.fusion.service.enums.PSIActuatorStatus', 'com.welab.wefe.data.fusion.service.utils.FusionUtils', 'com.welab.wefe.data.fusion.service.utils.bf.BloomFilters', 'com.welab.wefe.fusion.core.utils.CryptoUtils', 'com.welab.wefe.fusion.core.utils.PSIUtils', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.DataOutputStream', 'java.io.IOException', 'java.math.BigInteger', 'java.net.InetAddress', 'java.net.ServerSocket', 'java.net.Socket', 'java.util.ArrayList', 'java.util.HashMap', 'java.util.List', 'java.util.Map'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| PsiServerActuator | class |  |



## 类 PsiServerActuator

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | PsiServerActuator |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| threadId = new ThreadLocal<>() | ThreadLocal<Integer> |  |
| e | BigInteger |  |
| cacheMap = new HashMap<>() | Map<Integer, byte[][]> |  |
| d | BigInteger |  |
| serverSocket | ServerSocket |  |
| N | BigInteger |  |
| LOG = LoggerFactory.getLogger(PsiServerActuator.class) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




