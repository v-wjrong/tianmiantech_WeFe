# 基础信息

|      |      |
|------|------|
| 名称 | SecretUtil |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/fieldvalidate/secret/SecretUtil.java |
| 包名 | com.welab.wefe.common.fieldvalidate.secret |
| 依赖项 | ['com.welab.wefe.common.util.ClassUtils', 'com.welab.wefe.common.util.StringUtil', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.lang.reflect.Field', 'java.security.Security', 'java.util.HashMap', 'java.util.Map', 'java.util.Set'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| SecretUtil | class |  |



## 类 SecretUtil

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | SecretUtil |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| LOG = LoggerFactory.getLogger(Security.class) | Logger |  |
| SECRET_FIELD_MAP = new HashMap<>() | Map<Class, Map<String, Secret>> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| extractSecret | void |  |
| getAnnotation | Secret |  |




