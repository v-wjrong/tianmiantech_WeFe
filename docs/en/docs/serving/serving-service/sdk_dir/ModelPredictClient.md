# Basic Information

|      |      |
|------|------|
| Name | ModelPredictClient |
| Language | .java |
| Code Path | WeFe/serving/serving-service/sdk_dir/ModelPredictClient.java |
| Package Name | com.welab.wefe.mpc |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'java.io', 'java.math.BigInteger', 'java.net', 'java.nio.charset.StandardCharsets', 'java.security.KeyFactory', 'java.security.Signature', 'java.security.interfaces.RSAPrivateKey', 'java.security.spec.PKCS8EncodedKeySpec', 'java.util'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ModelPredictClient | class |  |



## Class ModelPredictClient

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ModelPredictClient |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| customer_privateKey = "***" | String |  |
| serviceId = "***" | String |  |
| customer_publicKey = "***" | String |  |
| api = "{{baseUrl}}/api/predict/%s" | String |  |
| customer_code = "***" | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| main | void |  |
| signRsa | String |  |
| sendPost | String |  |
| setFederatedPredictBody | String |  |




