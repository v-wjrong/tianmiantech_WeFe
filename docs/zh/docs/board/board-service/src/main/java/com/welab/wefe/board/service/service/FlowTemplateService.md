# 基础信息

|      |      |
|------|------|
| 名称 | FlowTemplateService |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/FlowTemplateService.java |
| 包名 | com.welab.wefe.board.service.service |
| 依赖项 | ['com.welab.wefe.board.service.api.project.flow.SaveFlowTemplateApi.Input', 'com.welab.wefe.board.service.database.entity.flow.FlowTemplateMySqlModel', 'com.welab.wefe.board.service.database.repository.FlowTemplateRepository', 'com.welab.wefe.common.data.mysql.Where', 'com.welab.wefe.common.web.util.CurrentAccountUtil', 'org.springframework.beans.factory.annotation.Autowired', 'org.springframework.data.jpa.domain.Specification', 'org.springframework.stereotype.Service', 'java.util.List'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| FlowTemplateService | class |  |



## 类 FlowTemplateService

|      |      |
|------|------|
| 访问范围 | @Service;public |
| 类型 | class |
| 名称 | FlowTemplateService |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| flowTemplateRepository | FlowTemplateRepository |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| addTemplate | String |  |
| save | FlowTemplateMySqlModel |  |
| query | List<FlowTemplateMySqlModel> |  |
| findById | FlowTemplateMySqlModel |  |




