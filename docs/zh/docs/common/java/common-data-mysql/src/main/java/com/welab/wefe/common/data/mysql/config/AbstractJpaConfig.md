# 基础信息

|      |      |
|------|------|
| 名称 | AbstractJpaConfig |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-mysql/src/main/java/com/welab/wefe/common/data/mysql/config/AbstractJpaConfig.java |
| 包名 | com.welab.wefe.common.data.mysql.config |
| 依赖项 | ['com.alibaba.druid.pool.DruidDataSource', 'com.alibaba.druid.spring.boot.autoconfigure.DruidDataSourceBuilder', 'com.welab.wefe.common.data.mysql.sql_monitor.SqlMonitor', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.boot.autoconfigure.orm.jpa.JpaProperties', 'org.springframework.boot.orm.jpa.EntityManagerFactoryBuilder', 'org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean', 'javax.sql.DataSource', 'java.util.Collections'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| AbstractJpaConfig | class |  |



## 类 AbstractJpaConfig

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | AbstractJpaConfig |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| mProperties | JpaProperties |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| entityManagerFactoryRef | LocalContainerEntityManagerFactoryBean |  |
| createDatasource | DataSource |  |




