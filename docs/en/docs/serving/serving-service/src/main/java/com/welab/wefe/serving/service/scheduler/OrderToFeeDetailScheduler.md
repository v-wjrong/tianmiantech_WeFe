# Basic Information

|      |      |
|------|------|
| Name | OrderToFeeDetailScheduler |
| Language | .java |
| Code Path | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/scheduler/OrderToFeeDetailScheduler.java |
| Package Name | com.welab.wefe.serving.service.scheduler |
| Dependencies | ['java.math.BigDecimal', 'java.util.ArrayList', 'java.util.Calendar', 'java.util.Date', 'java.util.List', 'java.util.Map', 'java.util.TimeZone', 'java.util.stream.Collectors', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.scheduling.annotation.Scheduled', 'org.springframework.stereotype.Component', 'com.welab.wefe.common.util.DateUtil', 'com.welab.wefe.common.util.HostUtil', 'com.welab.wefe.serving.service.database.entity.ClientServiceMysqlModel', 'com.welab.wefe.serving.service.database.entity.FeeConfigMysqlModel', 'com.welab.wefe.serving.service.database.entity.FeeDetailMysqlModel', 'com.welab.wefe.serving.service.database.entity.PartnerMysqlModel', 'com.welab.wefe.serving.service.database.entity.ServiceOrderMysqlModel', 'com.welab.wefe.serving.service.dto.ServiceOrderInput', 'com.welab.wefe.serving.service.enums.CallByMeEnum', 'com.welab.wefe.serving.service.enums.ServiceOrderEnum', 'com.welab.wefe.serving.service.service.ClientServiceService', 'com.welab.wefe.serving.service.service.FeeConfigService', 'com.welab.wefe.serving.service.service.FeeDetailService', 'com.welab.wefe.serving.service.service.PartnerService', 'com.welab.wefe.serving.service.service.ServiceOrderService'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| OrderToFeeDetailScheduler | class |  |



## Class OrderToFeeDetailScheduler

|      |      |
|------|------|
| Access Modifier | @Component;public |
| Type | class |
| Name | OrderToFeeDetailScheduler |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| clientServiceService | ClientServiceService |  |
| feeDetailService | FeeDetailService |  |
| feeConfigService | FeeConfigService |  |
| logger = LoggerFactory.getLogger(OrderToFeeDetailScheduler.class) | Logger |  |
| serviceOrderService | ServiceOrderService |  |
| partnerService | PartnerService |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| feeRecord | void |  |




