# Basic Information

|      |      |
|------|------|
| Name | CreateTestDataSetApi |
| Language | .java |
| Code Path | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common/web/api/dev/CreateTestDataSetApi.java |
| Package Name | com.welab.wefe.common.web.api.dev |
| Dependencies | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.OS', 'com.welab.wefe.common.util.RandomUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.config.CommonConfig', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'org.apache.commons.io.FileUtils', 'org.springframework.beans.factory.annotation.Autowired', 'java.io.File', 'java.io.FileOutputStream', 'java.io.IOException', 'java.nio.file.Path', 'java.nio.file.Paths', 'java.text.NumberFormat', 'java.util', 'java.util.stream.Collectors'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| CreateTestDataSetApi | class |  |



## Class CreateTestDataSetApi

|      |      |
|------|------|
| Access Modifier | @Api(path = "test/create_data_set", name = "generate data set for testing");public |
| Type | class |
| Name | CreateTestDataSetApi |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| PHONE_NUMBER_PREFIX = {"139", "138", "137", "136", "135", "134", "159", "158", "157", "150", "151", "152", "188", "187", "182", "183", "184", "178", "130", "131", "132", "156", "155", "186", "185", "176", "133", "153", "189", "180", "181", "177"} | String[] |  |
| commonConfig | CommonConfig |  |
| random = new Random() | Random |  |
| NUMBER_FORMAT = NumberFormat.getInstance() | NumberFormat |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| buildFeaturesConfig | Map<String, Feature> |  |
| createCnid | String |  |
| createPhoneNumber | String |  |
| createCsv | String |  |
| createValue | String |  |
| handle | ApiResult<Output> |  |
| createId | String |  |




