# 基础信息

|      |      |
|------|------|
| 名称 | AbstractApiInput |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/dto/AbstractApiInput.java |
| 包名 | com.welab.wefe.common.web.dto |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.alibaba.fastjson.annotation.JSONField', 'com.welab.wefe.common.Stopwatch', 'com.welab.wefe.common.fieldvalidate.AbstractCheckModel', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'javax.servlet.http.HttpServletRequest'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractApiInput | class |  |



## 类 AbstractApiInput

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | AbstractApiInput |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| request | HttpServletRequest |  |
| rawRequestParams | JSONObject |  |
| method | String |  |
| stopwatch = Stopwatch.startNew() | Stopwatch |  |
| callerMemberInfo | GatewayMemberInfo |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| clone | Object |  |
| fromGateway | boolean |  |




