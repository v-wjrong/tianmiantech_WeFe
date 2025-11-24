# Basic Information

|      |      |
|------|------|
| Name | ApiResult |
| Language | .java |
| Code Path | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/dto/ApiResult.java |
| Package Name | com.welab.wefe.common.web.dto |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.annotation.JSONField', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.fastjson.LoggerValueFilter'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ApiResult | class |  |



## Class ApiResult

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ApiResult |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| message | String |  |
| code = 0 | int |  |
| data | T |  |
| httpCode = 200 | int |  |
| spend | long |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getSpend | long |  |
| setSpend | void |  |
| ofErrorWithStatusCode | ApiResult<T> |  |
| getCode | int |  |
| success | boolean |  |
| setMessage | ApiResult<T> |  |
| setHttpCode | ApiResult<T> |  |
| ofSuccess | ApiResult<T> |  |
| toLogString | String |  |
| setCode | void |  |
| ofErrorWithStatusCode | ApiResult<T> |  |
| getMessage | String |  |
| getData | T |  |
| setData | void |  |




