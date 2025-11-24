# Basic Information

|      |      |
|------|------|
| Name | CommunicationConfig |
| Language | .java |
| Code Path | WeFe/mpc/mpc-common/src/main/java/com/welab/wefe/mpc/config/CommunicationConfig.java |
| Package Name | com.welab.wefe.mpc.config |
| Dependencies | ['java.util.UUID'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CommunicationConfig | class |  |



## Class CommunicationConfig

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | CommunicationConfig |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| serverUrl | String |  |
| secretKeyType | String |  |
| requestId = UUID.randomUUID().toString().replaceAll("-", "") | String |  |
| commercialId | String |  |
| signPrivateKey | String |  |
| apiName | String |  |
| needSign = true | boolean |  |

### Method List

| Name  | Type  | Description |
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




