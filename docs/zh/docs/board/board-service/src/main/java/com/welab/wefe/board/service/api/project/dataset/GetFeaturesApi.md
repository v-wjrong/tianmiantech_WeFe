# 基础信息

|      |      |
|------|------|
| 名称 | GetFeaturesApi |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/api/project/dataset/GetFeaturesApi.java |
| 包名 | com.welab.wefe.board.service.api.project.dataset |
| 依赖项 | ['com.welab.wefe.board.service.dto.vo.FeatureOutput', 'com.welab.wefe.board.service.service.DataSetColumnService', 'com.welab.wefe.common.fieldvalidate.annotation.Check', 'com.welab.wefe.common.web.api.base.AbstractApi', 'com.welab.wefe.common.web.api.base.Api', 'com.welab.wefe.common.web.dto.AbstractApiInput', 'com.welab.wefe.common.web.dto.ApiResult', 'org.springframework.beans.factory.annotation.Autowired', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| GetFeaturesApi | class |  |



## 类 GetFeaturesApi

|      |      |
|------|------|
| 访问范围 | @Api(path = "project/table_data_set/feature/list",;        name = "获取项目中数据集的特征列表",;        desc = "这里返回的特征列表会包含特征的数据类型，这个信息在union中不存在，所以需要额外获取。",;        allowAccessWithSign = true;);public |
| 类型 | class |
| 名称 | GetFeaturesApi |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| dataSetColumnService | DataSetColumnService |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| handle | ApiResult<GetFeaturesApi.Output> |  |




