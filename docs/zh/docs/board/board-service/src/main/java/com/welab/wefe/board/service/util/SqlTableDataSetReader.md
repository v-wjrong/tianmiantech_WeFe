# 基础信息

|      |      |
|------|------|
| 名称 | SqlTableDataSetReader |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/util/SqlTableDataSetReader.java |
| 包名 | com.welab.wefe.board.service.util |
| 依赖项 | ['com.welab.wefe.board.service.dto.entity.data_set.DataSetColumnInputModel', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.jdbc.JdbcClient', 'com.welab.wefe.common.jdbc.base.JdbcScanner', 'org.apache.commons.collections4.CollectionUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.IOException', 'java.util.LinkedHashMap', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| SqlTableDataSetReader | class |  |



## 类 SqlTableDataSetReader

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | SqlTableDataSetReader |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| sql | String |  |
| LOG = LoggerFactory.getLogger(SqlTableDataSetReader.class) | Logger |  |
| jdbcClient | JdbcClient |  |
| scanner | JdbcScanner |  |
| totalRowCount = -1 | long |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| close | void |  |
| readOneRow | LinkedHashMap<String, Object> |  |
| doGetHeader | List<String> |  |
| getTotalDataRowCount | long |  |




