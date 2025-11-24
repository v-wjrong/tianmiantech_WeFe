# 基础信息

|      |      |
|------|------|
| 名称 | CreateTestDataSetApi |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/api/dev/CreateTestDataSetApi.java |
| 包名 | com.welab.wefe.common.web.api.dev |
| 依赖项 | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.OS', 'com.welab.wefe.common.util.RandomUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.config.CommonConfig', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'org.apache.commons.io.FileUtils', 'org.springframework.beans.factory.annotation.Autowired', 'java.io.File', 'java.io.FileOutputStream', 'java.io.IOException', 'java.nio.file.Path', 'java.nio.file.Paths', 'java.text.NumberFormat', 'java.util', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| CreateTestDataSetApi | class |  |



## 类 CreateTestDataSetApi

|      |      |
|------|------|
| 访问范围 | @Api(path = "test/create_data_set", name = "generate data set for testing");public |
| 类型 | class |
| 名称 | CreateTestDataSetApi |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| PHONE_NUMBER_PREFIX = {"139", "138", "137", "136", "135", "134", "159", "158", "157", "150", "151", "152", "188", "187", "182", "183", "184", "178", "130", "131", "132", "156", "155", "186", "185", "176", "133", "153", "189", "180", "181", "177"} | String[] |  |
| commonConfig | CommonConfig |  |
| random = new Random() | Random |  |
| NUMBER_FORMAT = NumberFormat.getInstance() | NumberFormat |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| buildFeaturesConfig | Map<String, Feature> |  |
| createCnid | String |  |
| createPhoneNumber | String |  |
| createCsv | String |  |
| createValue | String |  |
| handle | ApiResult<Output> |  |
| createId | String |  |




