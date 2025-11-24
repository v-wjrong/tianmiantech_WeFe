# Basic Information

|      |      |
|------|------|
| Name | ConfigurationManager |
| Language | .java |
| Code Path | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/configuration/ConfigurationManager.java |
| Package Name | com.welab.wefe.common.configuration |
| Dependencies | ['com.welab.wefe.common.util.StringUtil', 'org.apache.commons.configuration', 'org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.File', 'java.nio.file.Files', 'java.nio.file.Paths', 'java.util.ArrayList', 'java.util.Arrays', 'java.util.List'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| ConfigurationManager | class |  |



## Class ConfigurationManager

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | ConfigurationManager |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| throwExceptionOnMissing = true | boolean |  |
| LOG = LoggerFactory.getLogger(ConfigurationManager.class) | Logger |  |
| configurationManager | ConfigurationManager |  |
| CONFIG_FILE = "configFile" | String |  |
| propertiesFiles = new ArrayList<>() | List<String> |  |
| config = new CompositeConfiguration() | CompositeConfiguration |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| init | void |  |
| init | void |  |
| getConfig | CompositeConfiguration |  |
| config | Configuration |  |
| addPropertyFiles | void |  |




