# 基础信息

|      |      |
|------|------|
| 名称 | ConfigurationManager |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/configuration/ConfigurationManager.java |
| 包名 | com.welab.wefe.common.configuration |
| 依赖项 | ['com.welab.wefe.common.util.StringUtil', 'org.apache.commons.configuration', 'org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.File', 'java.nio.file.Files', 'java.nio.file.Paths', 'java.util.ArrayList', 'java.util.Arrays', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ConfigurationManager | class |  |



## 类 ConfigurationManager

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | ConfigurationManager |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| throwExceptionOnMissing = true | boolean |  |
| LOG = LoggerFactory.getLogger(ConfigurationManager.class) | Logger |  |
| configurationManager | ConfigurationManager |  |
| CONFIG_FILE = "configFile" | String |  |
| propertiesFiles = new ArrayList<>() | List<String> |  |
| config = new CompositeConfiguration() | CompositeConfiguration |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| init | void |  |
| init | void |  |
| getConfig | CompositeConfiguration |  |
| config | Configuration |  |
| addPropertyFiles | void |  |




