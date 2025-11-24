# 基础信息

|      |      |
|------|------|
| 名称 | AbstractStorage |
| 编码语言 | .java |
| 代码路径 | WeFe/fusion/fusion-service/src/main/java/com/welab/wefe/data/fusion/service/repo/AbstractStorage.java |
| 包名 | com.welab.wefe.data.fusion.service.repo |
| 依赖项 | ['org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.beans.factory.annotation.Qualifier', 'javax.sql.DataSource', 'java.sql'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractStorage | class |  |



## 类 AbstractStorage

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | AbstractStorage |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| dataSource | DataSource |  |
| HEX_ARRAY = "0123456789ABCDEF".toCharArray() | char[] |  |
| LOG = LoggerFactory.getLogger(this.getClass()) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getCountByByteSize | int |  |
| getConnection | Connection |  |
| close | void |  |
| checkTB | void |  |
| close | void |  |
| formatTableName | String |  |




