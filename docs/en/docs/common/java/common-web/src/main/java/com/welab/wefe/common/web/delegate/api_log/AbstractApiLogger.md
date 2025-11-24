# Basic Information

|      |      |
|------|------|
| Name | AbstractApiLogger |
| Language | .java |
| Code Path | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/delegate/api_log/AbstractApiLogger.java |
| Package Name | com.welab.wefe.common.web.delegate.api_log |
| Dependencies | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.fastjson.LoggerValueFilter', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.ApiResult', 'com.welab.wefe.common.web.function.AfterApiExecuteFunction', 'com.welab.wefe.common.web.service.account.AccountInfo', 'com.welab.wefe.common.web.util.HttpServletRequestUtil', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'javax.servlet.http.HttpServletRequest', 'java.util.ArrayList', 'java.util.Date', 'java.util.List', 'java.util.concurrent.ConcurrentHashMap', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractApiLogger | class |  |



## Class AbstractApiLogger

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractApiLogger |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| IGNORE_LOG_APIS = new ArrayList<>() | List<String> |  |
| ACCOUNT_LAST_ACTION_TIME_MAP = new ConcurrentHashMap() | ConcurrentHashMap<String, Date> |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| logAccountLastActionTime | void |  |
| ignoreWithoutLogin | boolean |  |
| updateAccountLastActionTime | void |  |
| save | void |  |
| getIgnoreLogApiList | List<Class<? extends AbstractApi>> |  |
| action | void |  |
| beforeSaveLog | JSONObject |  |
| saveLog | void |  |
| ignore | boolean |  |




