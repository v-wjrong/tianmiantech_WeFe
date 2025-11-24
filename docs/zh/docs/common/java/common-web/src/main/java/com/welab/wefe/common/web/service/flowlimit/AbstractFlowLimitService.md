# 基础信息

|      |      |
|------|------|
| 名称 | AbstractFlowLimitService |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/service/flowlimit/AbstractFlowLimitService.java |
| 包名 | com.welab.wefe.common.web.service.flowlimit |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.wefe.enums.FlowLimitStrategyTypeEnum', 'javax.servlet.http.HttpServletRequest'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractFlowLimitService | class |  |



## 类 AbstractFlowLimitService

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | AbstractFlowLimitService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| httpServletRequest | HttpServletRequest |  |
| api | AbstractApi<?, ?> |  |
| params | JSONObject |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getApi | AbstractApi<?, ?> |  |
| setHttpServletRequest | void |  |
| setApi | void |  |
| getParams | JSONObject |  |
| setParams | void |  |
| getFlowLimitSecond | long |  |
| updateFlowLimit | void |  |
| getFlowLimitCount | int |  |
| getFlowLimitStrategyValue | String |  |
| getFlowLimitExceptionTips | String |  |
| getFlowLimit | FlowLimit |  |
| getHttpServletRequest | HttpServletRequest |  |
| check | void |  |
| getFlowLimitStrategyType | FlowLimitStrategyTypeEnum |  |
| getFlowLimitKey | String |  |
| createFlowLimit | FlowLimit |  |




