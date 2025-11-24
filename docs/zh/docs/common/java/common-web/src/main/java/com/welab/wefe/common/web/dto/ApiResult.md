# 基础信息

|      |      |
|------|------|
| 名称 | ApiResult |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/dto/ApiResult.java |
| 包名 | com.welab.wefe.common.web.dto |
| 依赖项 | ['com.alibaba.fastjson.JSON', 'com.alibaba.fastjson.annotation.JSONField', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.fastjson.LoggerValueFilter'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ApiResult | class |  |



## 类 ApiResult

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ApiResult |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| message | String |  |
| code = 0 | int |  |
| data | T |  |
| httpCode = 200 | int |  |
| spend | long |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




