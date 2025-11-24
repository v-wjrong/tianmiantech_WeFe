# Basic Information

|      |      |
|------|------|
| Name | Psi |
| Language | .java |
| Code Path | WeFe/mpc/mpc-psi/mpc-psi-sdk/src/main/java/com/welab/wefe/mpc/psi/sdk/Psi.java |
| Package Name | com.welab.wefe.mpc.psi.sdk |
| Dependencies | ['java.nio.charset.Charset', 'java.nio.file.Paths', 'java.util.ArrayList', 'java.util.Collection', 'java.util.Collections', 'java.util.HashMap', 'java.util.HashSet', 'java.util.Iterator', 'java.util.LinkedHashMap', 'java.util.LinkedList', 'java.util.List', 'java.util.Map', 'java.util.Random', 'java.util.Set', 'java.util.concurrent.ConcurrentHashMap', 'java.util.concurrent.ExecutorService', 'java.util.concurrent.Executors', 'java.util.concurrent.TimeUnit', 'org.apache.commons.collections4.CollectionUtils', 'org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.mpc.config.CommunicationConfig', 'com.welab.wefe.mpc.psi.request.QueryPrivateSetIntersectionRequest', 'com.welab.wefe.mpc.psi.request.QueryPrivateSetIntersectionResponse', 'com.welab.wefe.mpc.psi.sdk.model.ConfuseData', 'com.welab.wefe.mpc.psi.sdk.pir.PirQuery', 'com.welab.wefe.mpc.psi.sdk.service.PrivateSetIntersectionService', 'cn.hutool.core.io.FileUtil'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| Psi | class |  |



## Class Psi

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | Psi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| DEFAULT_BATCH_SIZE = -1 | int |  |
| PSI_RESULT_BY_PIR = "PSI_RESULT_BY_PIR" | String |  |
| needReturnFields = false | boolean |  |
| DEFAULT_CURRENT_BATCH = 0 | int |  |
| pushResultToServer = false | boolean |  |
| SAVE_RESULT_DIR = System.getProperty("user.dir") | String |  |
| isContinue | boolean |  |
| PUSH_RESULT_TO_SERVER = "PUSH_RESULT_TO_SERVER" | String |  |
| DH_PSI = "DH_PSI" | String |  |
| ECDH_PSI = "ECDH_PSI" | String |  |
| PSI_RESULT = "PSI_RESULT" | String |  |
| logger = LoggerFactory.getLogger(this.getClass()) | Logger |  |
| confuseData | ConfuseData |  |
| clientDatasetMap = new LinkedHashMap<>() | Map<String, String> |  |
| usePirToReturnFields = true | boolean |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| query | List<String> |  |
| isNeedReturnFields | boolean |  |
| readLastCurrentBatchAndSize | int[] |  |
| savePsiResult | void |  |
| returnFields | void |  |
| pushResultToServer | void |  |
| filterConfuseData | Set<String> |  |
| getClientDatasetMap | Map<String, String> |  |
| readPsiResult | List<String> |  |
| saveFieldResult | void |  |
| returnFieldsByPir | List<String> |  |
| setConfuseData | void |  |
| returnFieldsByCommon | List<String> |  |
| query | List<String> |  |
| setNeedReturnFields | void |  |
| query | List<String> |  |
| getConfuseData | ConfuseData |  |
| saveLastCurrentBatchAndSize | void |  |
| isContinue | boolean |  |
| setContinue | void |  |
| isUsePirToReturnFields | boolean |  |
| setUsePirToReturnFields | void |  |
| isPushResultToServer | boolean |  |
| setPushResultToServer | void |  |
| saveInCsv | void |  |
| setClientDatasetMap | void |  |




