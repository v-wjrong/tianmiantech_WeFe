# Basic Information

|      |      |
|------|------|
| Name | AbstractStorage |
| Language | .java |
| Code Path | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/repo/AbstractStorage.java |
| Package Name | com.welab.wefe.data.fusion.service.repo |
| Dependencies | ['org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.beans.factory.annotation.Qualifier', 'javax.sql.DataSource', 'java.sql'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractStorage | class |  |



## Class AbstractStorage

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractStorage |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| dataSource | DataSource |  |
| HEX_ARRAY = "0123456789ABCDEF".toCharArray() | char[] |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| getCountByByteSize | int |  |
| getConnection | Connection |  |
| close | void |  |
| checkTB | void |  |
| close | void |  |
| formatTableName | String |  |




