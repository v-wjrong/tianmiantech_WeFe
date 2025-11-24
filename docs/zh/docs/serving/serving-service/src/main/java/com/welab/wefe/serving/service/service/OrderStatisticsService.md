# 基础信息

|      |      |
|------|------|
| 名称 | OrderStatisticsService |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/service/OrderStatisticsService.java |
| 包名 | com.welab.wefe.serving.service.service |
| 依赖项 | ['com.alibaba.fastjson.JSON', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.StringUtil', 'com.welab.wefe.common.web.util.ModelMapper', 'com.welab.wefe.serving.service.api.orderstatistics.DownloadApi', 'com.welab.wefe.serving.service.api.orderstatistics.QueryListApi', 'com.welab.wefe.serving.service.api.orderstatistics.SaveApi', 'com.welab.wefe.serving.service.config.Config', 'com.welab.wefe.serving.service.database.entity.OrderStatisticsMysqlModel', 'com.welab.wefe.serving.service.database.repository.OrderStatisticsRepository', 'com.welab.wefe.serving.service.dto.OrderStatisticsInput', 'com.welab.wefe.serving.service.dto.PagingOutput', 'com.welab.wefe.serving.service.enums.DateTypeEnum', 'de.siegmar.fastcsv.writer.CsvWriter', 'de.siegmar.fastcsv.writer.LineDelimiter', 'de.siegmar.fastcsv.writer.QuoteStrategy', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'org.springframework.transaction.annotation.Transactional', 'java.io', 'java.nio.charset.StandardCharsets', 'java.util.ArrayList', 'java.util.Date', 'java.util.List', 'java.util.Map'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| OrderStatisticsService | class |  |



## 类 OrderStatisticsService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | OrderStatisticsService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| orderStatisticsRepository | OrderStatisticsRepository |  |
| log = LoggerFactory.getLogger(OrderStatisticsService.class) | Logger |  |
| config | Config |  |
| filePrefix = "order_statistics/" | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| downloadFile | File |  |
| save | void |  |
| insertList | void |  |
| writeCSV | File |  |
| queryList | PagingOutput<QueryListApi.Output> |  |
| insert | void |  |
| getLastRecord | OrderStatisticsMysqlModel |  |
| getByParams | List<OrderStatisticsMysqlModel> |  |




