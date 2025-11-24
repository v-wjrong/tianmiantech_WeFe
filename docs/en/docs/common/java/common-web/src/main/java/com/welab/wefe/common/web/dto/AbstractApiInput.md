# Basic Information

|      |      |
|------|------|
| Name | AbstractApiInput |
| Language | .java |
| Code Path | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/dto/AbstractApiInput.java |
| Package Name | com.welab.wefe.common.web.dto |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.alibaba.fastjson.annotation.JSONField', 'com.welab.wefe.common.Stopwatch', 'com.welab.wefe.common.fieldvalidate.AbstractCheckModel', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'javax.servlet.http.HttpServletRequest'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractApiInput | class |  |



## Class AbstractApiInput

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | AbstractApiInput |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| request | HttpServletRequest |  |
| rawRequestParams | JSONObject |  |
| method | String |  |
| stopwatch = Stopwatch.startNew() | Stopwatch |  |
| callerMemberInfo | GatewayMemberInfo |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| clone | Object |  |
| fromGateway | boolean |  |




