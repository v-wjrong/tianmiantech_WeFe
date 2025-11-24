# 基础信息

|      |      |
|------|------|
| 名称 | PsiClientActuator |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/actuator/rsapsi/PsiClientActuator.java |
| 包名 | com.welab.wefe.data.fusion.service.actuator.rsapsi |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.google.common.collect.Lists', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.Base64Util', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.data.fusion.service.dto.entity.PartnerOutputModel', 'com.welab.wefe.data.fusion.service.enums.ActionType', 'com.welab.wefe.data.fusion.service.enums.CallbackType', 'com.welab.wefe.data.fusion.service.enums.PSIActuatorStatus', 'com.welab.wefe.data.fusion.service.service.FieldInfoService', 'com.welab.wefe.data.fusion.service.service.ThirdPartyService', 'com.welab.wefe.data.fusion.service.service.dataset.DataSetService', 'com.welab.wefe.data.fusion.service.utils.FusionUtils', 'com.welab.wefe.data.fusion.service.utils.SocketUtils', 'com.welab.wefe.data.fusion.service.utils.bf.BitArray', 'com.welab.wefe.data.fusion.service.utils.bf.BloomFilters', 'com.welab.wefe.data.fusion.service.utils.primarykey.FieldInfo', 'com.welab.wefe.data.fusion.service.utils.primarykey.PrimaryKeyUtils', 'com.welab.wefe.fusion.core.utils.PSIUtils', 'org.apache.commons.collections4.CollectionUtils', 'java.io.DataInputStream', 'java.io.IOException', 'java.math.BigInteger', 'java.net.Socket', 'java.security.SecureRandom', 'java.util.ArrayList', 'java.util.HashMap', 'java.util.List', 'java.util.Map', 'java.util.concurrent'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| PsiClientActuator | class |  |



## 类 PsiClientActuator

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | PsiClientActuator |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| fieldInfoList | List<FieldInfo> |  |
| thirdPartyService = Launcher.CONTEXT.getBean(ThirdPartyService.class) | ThirdPartyService |  |
| columnList | List<String> |  |
| shard_size = 2000 | int |  |
| e | BigInteger |  |
| isTrace | Boolean |  |
| partnerModel | PartnerOutputModel |  |
| current_index = 0 | int |  |
| traceColumn | String |  |
| N | BigInteger |  |
| threadId = new ThreadLocal<>() | ThreadLocal<Integer> |  |
| rInv = new HashMap<>() | Map<Integer, List<BigInteger>> |  |
| cacheMap = new HashMap<>() | Map<Integer, List<JObject>> |  |
| threadPool = new ThreadPoolExecutor(            Runtime.getRuntime().availableProcessors(),            Runtime.getRuntime().availableProcessors() * 2,            100L,            TimeUnit.MILLISECONDS,            new LinkedBlockingQueue<>()) | ExecutorService |  |
| dataSetId | String |  |
| r = new HashMap<>() | Map<Integer, List<BigInteger>> |  |
| dataSetService = Launcher.CONTEXT.getBean(DataSetService.class) | DataSetService |  |
| data = new HashMap<>() | Map<Integer, List<String>> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| main | void |  |
| receiveAndParseResult | void |  |
| clear | void |  |
| cursor | boolean |  |
| downloadBloomFilter | void |  |
| generateBlindingFactor | BigInteger |  |
| fusion | void |  |
| query | void |  |
| align | void |  |
| execute | void |  |
| close | void |  |
| closeByHttp | void |  |
| init | void |  |
| handle | void |  |
| getPartnerModel | PartnerOutputModel |  |
| setPartnerModel | void |  |




