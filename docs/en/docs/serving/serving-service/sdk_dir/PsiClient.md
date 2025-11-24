# Basic Information

|      |      |
|------|------|
| Name | PsiClient |
| Language | .java |
| Code Path | WeFe/serving/serving-service/sdk_dir/PsiClient.java |
| Package Name | None |
| Dependencies | ['java.io.File', 'java.math.BigInteger', 'java.security.MessageDigest', 'java.util.ArrayList', 'java.util.Arrays', 'java.util.LinkedHashMap', 'java.util.LinkedList', 'java.util.List', 'java.util.Map', 'java.util.Random', 'com.alibaba.fastjson.JSONArray', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.mpc.config.CommunicationConfig', 'com.welab.wefe.mpc.psi.sdk.Psi', 'com.welab.wefe.mpc.psi.sdk.PsiFactory', 'com.welab.wefe.mpc.psi.sdk.excel.AbstractDataSetReader', 'com.welab.wefe.mpc.psi.sdk.excel.CsvDataSetReader', 'com.welab.wefe.mpc.psi.sdk.excel.ExcelDataSetReader', 'com.welab.wefe.mpc.psi.sdk.model.ConfuseData'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| PsiClient | class |  |



## Class PsiClient

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | PsiClient |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| clientDatasetMap | Map<String, String> |  |
| apiName = "api/*****" | String |  |
| Customer_code = "xxxx" | String |  |
| serverUrl = "http://xxxxx.com/xxxx/" | String |  |
| params = "[{\"field\":\"xxx\",\"operator\":\"xxx\"}]" | String |  |
| Customer_privateKey = "xxxx" | String |  |
| Customer_publicKey = "xxxx" | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getMD5String | String |  |
| calcKey | String |  |
| initClientDatasetByFile | void |  |
| main | void |  |
| init | void |  |
| generateConfuseData | ConfuseData |  |
| parseFieldsByParams | List<String> |  |
| getSHA256String | String |  |
| byte2Hex | String |  |




