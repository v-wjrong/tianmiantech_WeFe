# 基础信息

|      |      |
|------|------|
| 名称 | DataSetService |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/service/dataset/DataSetService.java |
| 包名 | com.welab.wefe.data.fusion.service.service.dataset |
| 依赖项 | ['com.welab.wefe.common.CommonThreadPool', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.jdbc.base.DatabaseType', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.data.fusion.service.api.dataset.DeleteApi', 'com.welab.wefe.data.fusion.service.api.dataset.PreviewApi', 'com.welab.wefe.data.fusion.service.api.dataset.QueryApi', 'com.welab.wefe.data.fusion.service.config.Config', 'com.welab.wefe.data.fusion.service.database.entity.DataSetMySqlModel', 'com.welab.wefe.data.fusion.service.database.entity.DataSourceMySqlModel', 'com.welab.wefe.data.fusion.service.database.repository.DataSetRepository', 'com.welab.wefe.data.fusion.service.database.repository.DataSourceRepository', 'com.welab.wefe.data.fusion.service.dto.base.PagingOutput', 'com.welab.wefe.data.fusion.service.dto.entity.dataset.DataSetDetailOutputModel', 'com.welab.wefe.data.fusion.service.dto.entity.dataset.DataSetOutputModel', 'com.welab.wefe.data.fusion.service.dto.entity.dataset.DataSetPreviewOutputModel', 'com.welab.wefe.data.fusion.service.enums.DataResourceSource', 'com.welab.wefe.data.fusion.service.manager.JdbcManager', 'com.welab.wefe.data.fusion.service.service.AbstractService', 'com.welab.wefe.data.fusion.service.service.DataStorageService', 'com.welab.wefe.data.fusion.service.utils.dataresouce.DataResouceHelper', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.beans.factory.annotation.Value', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.io.File', 'java.io.IOException', 'java.sql.Connection', 'java.sql.PreparedStatement', 'java.sql.ResultSet', 'java.sql.SQLException', 'java.util.ArrayList', 'java.util.Arrays', 'java.util.Date', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DataSetService | class |  |



## 类 DataSetService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | DataSetService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| config | Config |  |
| dataSetRepository | DataSetRepository |  |
| mySqlUsername | String |  |
| mySqlPassword | String |  |
| TABLE_HEADER = "data_fusion_" | String |  |
| dataSourceRepo | DataSourceRepository |  |
| mySqlUrl | String |  |
| dataStorageService | DataStorageService |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getDataSetFile | File |  |
| findById | DataSetMySqlModel |  |
| paging | List<JObject> |  |
| preview | DataSetPreviewOutputModel |  |
| delete | void |  |
| testSqlQuery | boolean |  |
| increment | void |  |
| detailAndPreview | DataSetDetailOutputModel |  |
| count | int |  |
| detail | DataSetOutputModel |  |
| query | PagingOutput<DataSetOutputModel> |  |
| getDataSourceById | DataSourceMySqlModel |  |
| list | List<DataSetMySqlModel> |  |




