# 基础信息

|      |      |
|------|------|
| 名称 | ImageDataSetSampleService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/data_resource/image_data_set/ImageDataSetSampleService.java |
| 包名 | com.welab.wefe.board.service.service.data_resource.image_data_set |
| 依赖项 | ['com.welab.wefe.board.service.api.data_resource.image_data_set.sample.ImageDataSetSampleQueryApi', 'com.welab.wefe.board.service.api.data_resource.image_data_set.sample.ImageDataSetSampleStatisticsApi', 'com.welab.wefe.board.service.api.data_resource.image_data_set.sample.ImageDataSetSampleUpdateApi', 'com.welab.wefe.board.service.database.entity.data_set.ImageDataSetSampleMysqlModel', 'com.welab.wefe.board.service.database.repository.ImageDataSetSampleRepository', 'com.welab.wefe.board.service.dto.base.PagingOutput', 'com.welab.wefe.board.service.dto.entity.data_set.ImageDataSetSampleOutputModel', 'com.welab.wefe.board.service.service.AbstractService', 'com.welab.wefe.common.StatusCode', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.exception.StatusCodeWithException', 'com.welab.wefe.common.util.FileUtil', 'com.welab.wefe.common.util.JObject', 'com.welab.wefe.common.util.MapUtil', 'com.welab.wefe.common.util.StringUtil', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.List', 'java.util.Map', 'java.util.TreeMap', 'java.util.stream.Collectors'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| ImageDataSetSampleService | class |  |



## 类 ImageDataSetSampleService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | ImageDataSetSampleService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| imageDataSetSampleRepository | ImageDataSetSampleRepository |  |
| imageDataSetService | ImageDataSetService |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| update | void |  |
| query | PagingOutput<ImageDataSetSampleOutputModel> |  |
| allLabeled | List<ImageDataSetSampleMysqlModel> |  |
| delete | void |  |
| statistics | ImageDataSetSampleStatisticsApi.Output |  |




