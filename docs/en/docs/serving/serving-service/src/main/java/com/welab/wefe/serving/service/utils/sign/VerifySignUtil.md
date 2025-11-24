# Basic Information

|      |      |
|------|------|
| Name | VerifySignUtil |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/utils/sign/VerifySignUtil.java |
| Package Name | com.welab.wefe.serving.service.utils.sign |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.web.api.base.Caller', 'javax.servlet.http.HttpServletRequest', 'java.util.HashMap', 'java.util.Map'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| VerifySignUtil | class |  |



## Class VerifySignUtil

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | VerifySignUtil |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| VERIFY_SIGN_FUNCTION_MAP = new HashMap<>() | Map<String, Class<? extends AbstractVerifySignFunction>> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getFunction | AbstractVerifySignFunction |  |
| rsaVerify | void |  |




