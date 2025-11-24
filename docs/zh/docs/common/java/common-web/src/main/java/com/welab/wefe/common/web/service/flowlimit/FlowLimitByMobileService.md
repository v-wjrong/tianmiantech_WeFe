# 基础信息

|      |      |
|------|------|
| 名称 | FlowLimitByMobileService |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/service/flowlimit/FlowLimitByMobileService.java |
| 包名 | com.welab.wefe.common.web.service.flowlimit |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.api.base.FlowLimitByMobile', 'com.welab.wefe.common.wefe.enums.FlowLimitStrategyTypeEnum', 'javax.servlet.http.HttpServletRequest', 'java.util.Arrays', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| FlowLimitByMobileService | class |  |



## 类 FlowLimitByMobileService

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | FlowLimitByMobileService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| PARAMS_MOBILE_KEY = Arrays.asList("mobile", "phoneNumber", "phone_number") | List<String> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getFlowLimitStrategyValue | String |  |
| getFlowLimitStrategyType | FlowLimitStrategyTypeEnum |  |
| getFlowLimitSecond | long |  |
| getFlowLimitKey | String |  |
| getFlowLimitCount | int |  |
| getFlowLimitExceptionTips | String |  |
| getMobile | String |  |




