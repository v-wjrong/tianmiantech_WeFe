# 基础信息

|      |      |
|------|------|
| 名称 | CommunicationConfig |
| 编码语言 | .java |
| 代码路径 | WeFe/mpc/mpc-common/src/main/java/com/welab/wefe/mpc/config/CommunicationConfig.java |
| 包名 | com.welab.wefe.mpc.config |
| 依赖项 | ['java.util.UUID'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CommunicationConfig | class |  |



## 类 CommunicationConfig

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | CommunicationConfig |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| serverUrl | String |  |
| secretKeyType | String |  |
| requestId = UUID.randomUUID().toString().replaceAll("-", "") | String |  |
| commercialId | String |  |
| signPrivateKey | String |  |
| apiName | String |  |
| needSign = true | boolean |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getSecretKeyType | String |  |
| setServerUrl | void |  |
| getServerUrl | String |  |
| setSignPrivateKey | void |  |
| getCommercialId | String |  |
| getSignPrivateKey | String |  |
| getRequestId | String |  |
| getApiName | String |  |
| setApiName | void |  |
| setRequestId | void |  |
| setCommercialId | void |  |
| isNeedSign | boolean |  |
| setNeedSign | void |  |
| setSecretKeyType | void |  |




