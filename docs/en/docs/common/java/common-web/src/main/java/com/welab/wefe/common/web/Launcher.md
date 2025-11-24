# Basic Information

|      |      |
|------|------|
| Name | Launcher |
| Language | .java |
| Code Path | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/Launcher.java |
| Package Name | com.welab.wefe.common.web |
| Dependencies | ['com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.delegate.api_log.AbstractApiLogger', 'com.welab.wefe.common.web.function', 'com.welab.wefe.common.web.service.CaptchaService', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.boot.SpringApplication', 'org.springframework.context.ApplicationContext', 'org.springframework.stereotype.Component', 'org.springframework.stereotype.Repository', 'org.springframework.stereotype.Service'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| Launcher | class |  |



## Class Launcher

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | Launcher |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| API_LOGGER | AbstractApiLogger |  |
| BEFORE_API_EXECUTE_FUNCTION | BeforeApiExecuteFunction |  |
| API_PACKAGE_PATH | String |  |
| AFTER_API_EXECUTE_FUNCTION | AfterApiExecuteFunction |  |
| FLOW_LIMIT_BY_MOBILE_FUNCTION | FlowLimitByMobileFunction |  |
| CHECK_SESSION_TOKEN_FUNCTION | CheckSessionTokenFunction |  |
| ON_API_EXCEPTION_FUNCTION | OnApiExceptionFunction |  |
| FLOW_LIMIT_BY_IP_FUNCTION | FlowLimitByIpFunction |  |
| LOG = LoggerFactory.getLogger(Launcher.class) | Logger |  |
| CONTEXT | ApplicationContext |  |
| API_PERMISSION_POLICY | ApiPermissionPolicyFunction |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| apiLogger | Launcher |  |
| checkSessionTokenFunction | Launcher |  |
| instance | Launcher |  |
| apiPermissionPolicy | Launcher |  |
| getBean | T |  |
| afterApiExecuteFunction | Launcher |  |
| onApiExceptionFunction | Launcher |  |
| beforeApiExecuteFunction | Launcher |  |
| launch | void |  |
| flowLimitByIpFunctionFunction | Launcher |  |
| flowLimitByMobileFunctionFunction | Launcher |  |
| apiPackagePath | Launcher |  |
| apiPackageClass | Launcher |  |




