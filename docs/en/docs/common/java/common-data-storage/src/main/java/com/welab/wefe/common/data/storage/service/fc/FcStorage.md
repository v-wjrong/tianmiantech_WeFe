# Basic Information

|      |      |
|------|------|
| Name | FcStorage |
| Language | .java |
| Code Path | WeFe/common/java/common-data-storage/src/main/java/com/welab/wefe/common/data/storage/service/fc/FcStorage.java |
| Package Name | com.welab.wefe.common.data.storage.service.fc |
| Dependencies | ['com.welab.wefe.common.data.storage.model.DataItemModel', 'com.welab.wefe.common.data.storage.service.fc.aliyun.AliyunOssConfig', 'com.welab.wefe.common.data.storage.service.fc.aliyun.AliyunOssStorage', 'com.welab.wefe.common.data.storage.service.fc.tencent.TencentCosConfig', 'com.welab.wefe.common.data.storage.service.fc.tencent.TencentCosStorage', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.util.List', 'java.util.Map'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| FcStorage | class |  |



## Class FcStorage

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | FcStorage |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| storage | FcStorage |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| putAll | void |  |
| initWithTencent | void |  |
| initWithAliyun | void |  |
| getInstance | FcStorage |  |




