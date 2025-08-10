[回到首页](../README.md)

## 项目概览
### 项目基本信息
- **名称:** wefe
- **GroupId (Maven):** com.welab.wefe
- **ArtifactId (Maven):** wefe
- **Version:** 1.0.0
- **主要编程语言:** Java

## 先决条件
- **JDK 版本:** 1.8（通过 Maven 的 `<java.version>1.8` 和 `<maven.compiler.source>/<target>` 配置明确指定）
- **构建工具版本:** Maven（通过 `pom.xml` 文件结构和 `<modelVersion>4.0.0</modelVersion>` 确认）
- **网络连接中间件依赖:**
  - **MySQL:** 8.0.27（`mysql-connector-java`）
  - **PostgreSQL:** 42.4.1（`postgresql`）
  - **MongoDB:** 通过 `spring-boot-starter-data-mongodb` 隐式依赖
  - **Hadoop:** 3.2.4（`hadoop-common`）和 2.7.4（`hadoop-client`）
  - **FISCO BCOS:** 2.8.0（`fisco-bcos-java-sdk`）
  - **Redis:** 通过 `jedis` 隐式依赖
  - **阿里云 OSS:** 3.8.0（`aliyun-sdk-oss`）
  - **阿里云 TableStore:** 5.4.0（`tablestore`）
  - **gRPC:** 1.29.0（`grpc-all` 和 `grpc-netty-shaded`）
  - **Hive:** 2.1.1（`hive-jdbc`）和 2.3.4（另一处 `hive-jdbc`）
  - **ClickHouse:** 0.2.5（`clickhouse-jdbc`）

## 构建指南
### Maven 构建
- 构建命令:
    - 清理构建: `mvn clean`
    - 编译项目: `mvn compile`
    - 打包项目: `mvn package`
    - 安装到本地仓库: `mvn install`
    - 部署项目: `mvn deploy`
- 构建流程: 
    - Maven 的构建流程主要包括以下阶段：
        1. 清理 (clean): 删除之前的构建输出
        2. 编译 (compile): 编译项目源代码
        3. 测试 (test): 运行单元测试
        4. 打包 (package): 将编译后的代码打包成可分发的格式（如 JAR、WAR）
        5. 验证 (verify): 运行任何检查以验证包是否有效
        6. 安装 (install): 将包安装到本地 Maven 仓库
        7. 部署 (deploy): 将最终包复制到远程仓库
- 打包目录: 
    - 打包后的文件通常位于 `target/` 目录下
    - 对于 Spring Boot 项目，可执行 JAR 文件会包含所有依赖
    - 模块化项目的每个子模块会有自己的 `target/` 目录
    - 最终打包文件名通常遵循 `<artifactId>-<version>.<packaging>` 的格式

### 项目特定说明
- 这是一个多模块 Maven 项目，包含多个子模块
- 主要模块包括: board, common, union, gateway, serving, fusion, mpc, manager
- 使用 Spring Boot 作为基础框架
- 使用 Maven profiles 区分本地(local)和生产(prod)环境
- 部分模块有自定义的打包配置和主类定义

## 依赖管理
### 主要依赖
- **Spring Boot**: 用于构建微服务应用，版本通过父项目 `spring-boot-starter-parent` 管理 (2.1.10.RELEASE)
- **数据库相关**:
  - MySQL: `mysql-connector-java` (8.0.27)
  - MongoDB: `spring-boot-starter-data-mongodb`
  - PostgreSQL: `postgresql` (42.4.1)
  - Hive: `hive-jdbc` (2.3.4)
- **工具库**:
  - Hutool: `hutool-core` (5.8.9)
  - Guava: `guava` (27.0.1-jre 和 30.0-jre)
  - Apache Commons: `commons-lang3` (3.10), `commons-collections4` (4.4), `commons-io` (2.7)
- **安全相关**:
  - Bouncy Castle: `bcpkix-jdk15on` 和 `bcprov-jdk15on` (1.60)
  - FISCO BCOS: `fisco-bcos-java-sdk` (2.8.0)
- **Web/网络**:
  - Spring Web: `spring-boot-starter-web`
  - HTTP Client: `httpclient` (4.5.12)
- **序列化/反序列化**:
  - Fastjson: `fastjson` (1.2.83)
  - Jackson: `jackson-databind` (2.9.10.7)
  - Protobuf: `protobuf-java` (3.16.1)
- **日志**:
  - SLF4J: `slf4j-log4j12` (1.7.15)
  - Logback: `logback-classic` (1.2.9)

### 添加/修改依赖
- **Maven:** 在 `pom.xml` 文件的 `<dependencies>` 标签中添加或修改 `<dependency>` 元素。例如：
  ```xml
  <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-web</artifactId>
  </dependency>
  ```

### 依赖版本管理
- **Maven (`<dependencyManagement>`):** 
  - 父项目 `wefe` 的 `pom.xml` 中通过 `<dependencyManagement>` 统一管理了多个依赖的版本，例如：
    ```xml
    <dependencyManagement>
        <dependencies>
            <dependency>
                <groupId>com.fasterxml.jackson.core</groupId>
                <artifactId>jackson-databind</artifactId>
                <version>${jackson-databind.version}</version>
            </dependency>
            <dependency>
                <groupId>mysql</groupId>
                <artifactId>mysql-connector-java</artifactId>
                <version>${mysql.connector.version}</version>
            </dependency>
        </dependencies>
    </dependencyManagement>
    ```
  - 版本号通过 `<properties>` 集中定义，例如：
    ```xml
    <properties>
        <mysql.connector.version>8.0.27</mysql.connector.version>
        <jackson-databind.version>2.9.10.7</jackson-databind.version>
    </properties>
    ```

