# Basic Information

|      |      |
|------|------|
| Name | DataSourceConfig |
| Language | .java |
| Code Path | WeFe/gateway/src/main/java/com/welab/wefe/gateway/config/DataSourceConfig.java |
| Package Name | com.welab.wefe.gateway.config |
| Dependencies | ['com.welab.wefe.common.data.mysql.config.AbstractJpaConfig', 'com.welab.wefe.gateway.GatewayServer', 'com.welab.wefe.gateway.entity.FlagEntity', 'org.springframework.beans.factory.annotation.Qualifier', 'org.springframework.boot.autoconfigure.domain.EntityScan', 'org.springframework.boot.context.properties.ConfigurationProperties', 'org.springframework.boot.orm.jpa.EntityManagerFactoryBuilder', 'org.springframework.context.annotation.Bean', 'org.springframework.context.annotation.Configuration', 'org.springframework.context.annotation.Primary', 'org.springframework.data.jpa.repository.config.EnableJpaRepositories', 'org.springframework.orm.jpa.JpaTransactionManager', 'org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean', 'org.springframework.transaction.PlatformTransactionManager', 'javax.sql.DataSource'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| DataSourceConfig | class |  |



## Class DataSourceConfig

|      |      |
|------|------|
| Access Modifier | @Configuration;@EntityScan("com.welab.gateway");@EnableJpaRepositories(basePackageClasses = GatewayServer.class,;        entityManagerFactoryRef = "entityManagerFactoryRefWefeGateway",;        transactionManagerRef = "transactionManagerRefWefeGateway");public |
| Type | class |
| Name | DataSourceConfig |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| wefeGatewayDS | DataSource |  |
| entityManagerFactoryRefWefeGateway | LocalContainerEntityManagerFactoryBean |  |
| transactionManagerRefWefeGateway | PlatformTransactionManager |  |




