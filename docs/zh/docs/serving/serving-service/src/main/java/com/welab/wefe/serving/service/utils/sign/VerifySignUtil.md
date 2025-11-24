# 基础信息

|      |      |
|------|------|
| 名称 | VerifySignUtil |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/utils/sign/VerifySignUtil.java |
| 包名 | com.welab.wefe.serving.service.utils.sign |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.web.api.base.Caller', 'javax.servlet.http.HttpServletRequest', 'java.util.HashMap', 'java.util.Map'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| VerifySignUtil | class |  |



## 类 VerifySignUtil

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | VerifySignUtil |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| VERIFY_SIGN_FUNCTION_MAP = new HashMap<>() | Map<String, Class<? extends AbstractVerifySignFunction>> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getFunction | AbstractVerifySignFunction |  |
| rsaVerify | void |  |




