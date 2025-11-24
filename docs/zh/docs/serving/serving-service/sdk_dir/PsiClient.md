# 基础信息

|      |      |
|------|------|
| 名称 | PsiClient |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/sdk_dir/PsiClient.java |
| 包名 | None |
| 依赖项 | ['java.io.File', 'java.math.BigInteger', 'java.security.MessageDigest', 'java.util.ArrayList', 'java.util.Arrays', 'java.util.LinkedHashMap', 'java.util.LinkedList', 'java.util.List', 'java.util.Map', 'java.util.Random', 'com.alibaba.fastjson.JSONArray', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.mpc.config.CommunicationConfig', 'com.welab.wefe.mpc.psi.sdk.Psi', 'com.welab.wefe.mpc.psi.sdk.PsiFactory', 'com.welab.wefe.mpc.psi.sdk.excel.AbstractDataSetReader', 'com.welab.wefe.mpc.psi.sdk.excel.CsvDataSetReader', 'com.welab.wefe.mpc.psi.sdk.excel.ExcelDataSetReader', 'com.welab.wefe.mpc.psi.sdk.model.ConfuseData'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| PsiClient | class |  |



## 类 PsiClient

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | PsiClient |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| clientDatasetMap | Map<String, String> |  |
| apiName = "api/*****" | String |  |
| Customer_code = "xxxx" | String |  |
| serverUrl = "http://xxxxx.com/xxxx/" | String |  |
| params = "[{\"field\":\"xxx\",\"operator\":\"xxx\"}]" | String |  |
| Customer_privateKey = "xxxx" | String |  |
| Customer_publicKey = "xxxx" | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
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




