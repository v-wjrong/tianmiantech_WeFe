# Basic Information

|      |      |
|------|------|
| Name | DataSourceService |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/DataSourceService.java |
| Package Name | com.welab.wefe.serving.service.service |
| Dependencies | ['com.alibaba.fastjson.JSONObject', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.jdbc.base.DatabaseType', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.serving.service.api.datasource', 'com.welab.wefe.serving.service.api.datasource.QueryTableFieldsApi.FieldOutput', 'com.welab.wefe.serving.service.api.datasource.QueryTablesApi.Output', 'com.welab.wefe.serving.service.database.entity.DataSourceMySqlModel', 'com.welab.wefe.serving.service.database.repository.DataSourceRepository', 'com.welab.wefe.serving.service.dto.PagingOutput', 'com.welab.wefe.serving.service.manager.JdbcManager', 'org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.sql.Connection', 'java.sql.SQLException', 'java.util'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataSourceService | class |  |



## Class DataSourceService

|      |      |
|------|------|
| Access Modifier | @Service;public |
| Type | class |
| Name | DataSourceService |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| dataSourceRepo | DataSourceRepository |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| query | PagingOutput<QueryApi.Output> |  |
| queryListByConditions | List<Map<String, String>> |  |
| batchInsert | void |  |
| queryTableFields | com.welab.wefe.serving.service.api.datasource.QueryTableFieldsApi.Output |  |
| getDataSourceById | DataSourceMySqlModel |  |
| testDBConnect | TestDBConnectApi.Output |  |
| queryList | List<Map<String, String>> |  |
| batchQuerySql | Map<String, String> |  |
| update | UpdateApi.DataSourceUpdateOutput |  |
| update | boolean |  |
| delete | void |  |
| queryTables | Output |  |
| queryListByIds | List<Map<String, String>> |  |
| createTable | void |  |
| findById | DataSourceMySqlModel |  |
| count | long |  |
| queryOne | Map<String, String> |  |
| add | AddApi.DataSourceAddOutput |  |




