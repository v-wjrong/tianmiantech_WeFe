# Basic Information

|      |      |
|------|------|
| Name | AbstractParser |
| Language | .java |
| Code Path | WeFe/union/blockchain-data-sync/src/main/java/com/welab/wefe/parser/AbstractParser.java |
| Package Name | com.welab.wefe.parser |
| Dependencies | ['com.alibaba.fastjson.JSONArray', 'com.alibaba.fastjson.JSONObject', 'com.welab.wefe.bo.data.EventBO', 'com.welab.wefe.constant.EventConstant', 'com.welab.wefe.exception.BusinessException', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| AbstractParser | class |  |



## Class AbstractParser

|      |      |
|------|------|
| Access Modifier | public abstract |
| Type | class |
| Name | AbstractParser |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| extJsonStr | String |  |
| params | JSONArray |  |
| log = LoggerFactory.getLogger(AbstractParser.class) | Logger |  |
| RET_CODE = "ret_code" | String |  |
| eventBO | EventBO |  |
| PARAMS = "params" | String |  |
| EXT_JSON = "ext_json" | String |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| parseContractEvent | void |  |
| process | void |  |




