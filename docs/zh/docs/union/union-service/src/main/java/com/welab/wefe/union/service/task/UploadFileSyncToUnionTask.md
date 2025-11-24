# 基础信息

|      |      |
|------|------|
| 名称 | UploadFileSyncToUnionTask |
| 编码语言 | .java |
| 代码路径 | WeFe/union/union-service/src/main/java/com/welab/wefe/union/service/task/UploadFileSyncToUnionTask.java |
| 包名 | com.welab.wefe.union.service.task |
| 依赖项 | ['com.alibaba.fastjson.JSONException', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.http.HttpContentType', 'com.welab.wefe.common.http.HttpRequest', 'com.welab.wefe.common.http.HttpResponse', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.SM2Util', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.util.ThreadUtil', 'com.welab.wefe.union.service.cache.UnionNodeConfigCache', 'org.apache.http.entity.ContentType', 'org.apache.http.entity.mime.content.InputStreamBody', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.util.MultiValueMap', 'org.springframework.web.multipart.MultipartFile', 'java.io.IOException', 'java.util.Map'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| UploadFileSyncToUnionTask | class |  |



## 类 UploadFileSyncToUnionTask

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | UploadFileSyncToUnionTask |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| fileStreamBodyMap | Map<String, InputStreamBody> |  |
| params | JObject |  |
| baseUrl | String |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |
| api | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| run | void |  |




