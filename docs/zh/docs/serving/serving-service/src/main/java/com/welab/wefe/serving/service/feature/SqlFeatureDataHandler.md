# 基础信息

|      |      |
|------|------|
| 名称 | SqlFeatureDataHandler |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/feature/SqlFeatureDataHandler.java |
| 包名 | com.welab.wefe.serving.service.feature |
| 依赖项 | ['com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.jdbc.base.DatabaseType', 'com.welab.wefe.common.web.Launcher', 'com.welab.wefe.serving.sdk.model.FeatureDataModel', 'com.welab.wefe.serving.service.database.entity.DataSourceMySqlModel', 'com.welab.wefe.serving.service.database.entity.TableModelMySqlModel', 'com.welab.wefe.serving.service.feature.sql.AbstractTemplate', 'com.welab.wefe.serving.service.feature.sql.SqlRuleUtil', 'com.welab.wefe.serving.service.feature.sql.hive.HiveTemplate', 'com.welab.wefe.serving.service.feature.sql.impala.ImpalaTemplate', 'com.welab.wefe.serving.service.feature.sql.mysql.MySqlTemplate', 'com.welab.wefe.serving.service.feature.sql.pg.PgSqlTemplate', 'com.welab.wefe.serving.service.service.DataSourceService', 'com.welab.wefe.serving.service.service.ModelService', 'java.util.HashMap', 'java.util.Map'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| SqlFeatureDataHandler | class |  |



## 类 SqlFeatureDataHandler

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | SqlFeatureDataHandler |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| modelService | ModelService |  |
| SQL_TEMPLATE = new HashMap<>() | Map<DatabaseType, GenerateTemplateFunction> |  |
| dataSourceService | DataSourceService |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getDataSourceMySqlModel | DataSourceMySqlModel |  |
| findSqlConfig | DataSourceMySqlModel |  |
| buildSqlContext | String |  |
| handle | FeatureDataModel |  |
| generateTemplate | AbstractTemplate |  |
| buildSqlContextByModelId | String |  |
| debug | FeatureDataModel |  |




