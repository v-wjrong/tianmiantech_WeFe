# Basic Information

|      |      |
|------|------|
| Name | SecretUtil |
| Language | .java |
| Code Path | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/fieldvalidate/secret/SecretUtil.java |
| Package Name | com.welab.wefe.common.fieldvalidate.secret |
| Dependencies | ['com.welab.wefe.common.util.ClassUtils', 'com.welab.wefe.common.util.StringUtil', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.lang.reflect.Field', 'java.security.Security', 'java.util.HashMap', 'java.util.Map', 'java.util.Set'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| SecretUtil | class |  |



## Class SecretUtil

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | SecretUtil |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(Security.class) | Logger |  |
| SECRET_FIELD_MAP = new HashMap<>() | Map<Class, Map<String, Secret>> |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| extractSecret | void |  |
| getAnnotation | Secret |  |




