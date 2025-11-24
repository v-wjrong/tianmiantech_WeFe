# 基础信息

|      |      |
|------|------|
| 名称 | Launcher |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/Launcher.java |
| 包名 | com.welab.wefe.common.web |
| 依赖项 | ['com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.delegate.api_log.AbstractApiLogger', 'com.welab.wefe.common.web.function', 'com.welab.wefe.common.web.service.CaptchaService', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.boot.SpringApplication', 'org.springframework.context.ApplicationContext', 'org.springframework.stereotype.Component', 'org.springframework.stereotype.Repository', 'org.springframework.stereotype.Service'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| Launcher | class |  |



## 类 Launcher

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | Launcher |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
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

### 方法列表

| 名称  | 类型  | 说明 |
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




