# 基础信息

|      |      |
|------|------|
| 名称 | ModelPredictClient |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/sdk_dir/ModelPredictClient.java |
| 包名 | com.welab.wefe.mpc |
| 依赖项 | ['com.alibaba.fastjson.JSONObject', 'java.io', 'java.math.BigInteger', 'java.net', 'java.nio.charset.StandardCharsets', 'java.security.KeyFactory', 'java.security.Signature', 'java.security.interfaces.RSAPrivateKey', 'java.security.spec.PKCS8EncodedKeySpec', 'java.util'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ModelPredictClient | class |  |



## 类 ModelPredictClient

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ModelPredictClient |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| customer_privateKey = "***" | String |  |
| serviceId = "***" | String |  |
| customer_publicKey = "***" | String |  |
| api = "{{baseUrl}}/api/predict/%s" | String |  |
| customer_code = "***" | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| main | void |  |
| signRsa | String |  |
| sendPost | String |  |
| setFederatedPredictBody | String |  |




