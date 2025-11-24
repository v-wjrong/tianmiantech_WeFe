# 基础信息

|      |      |
|------|------|
| 名称 | BaseXgboostLanguage |
| 编码语言 | .java |
| 代码路径 | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/modelexport/BaseXgboostLanguage.java |
| 包名 | com.welab.wefe.board.service.service.modelexport |
| 依赖项 | ['com.welab.wefe.common.util.JObject', 'org.apache.commons.collections4.CollectionUtils', 'java.util.ArrayList', 'java.util.LinkedHashMap', 'java.util.List', 'java.util.Map', 'java.util.regex.Matcher', 'java.util.regex.Pattern'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| BaseXgboostLanguage | class |  |



## 类 BaseXgboostLanguage

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | BaseXgboostLanguage |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| INDENTATION_UNIT_CHAR = "    " | String |  |
| MAX_LOOP_COUNT = 1000 | int |  |
| ROOT_NODE_KEY = "0" | String |  |
| SPECIAL_NUMERIC = "#" | String |  |
| METHOD_BODY_PLACEHOLDER = "#body#" | String |  |
| NUM_CLASSES_2_CLASSIFICATIONS = 2 | int |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| buildTreeVarNameList | List<String> |  |
| indentationByNodeLayer | String |  |
| indentationByNodeLayer | String |  |
| buildMethodResultLogicCode | String |  |
| generateResultVarName | String |  |
| generateIdPlaceholder | String |  |
| preBuild2ClassificationsMethodSignNameCode | String |  |
| generateVarName | String |  |
| buildMethodBodyCode | String |  |
| buildWholeCode | String |  |
| resultIndentationNum | String |  |
| build2ClassificationsReturnCode | String |  |
| buildMultipleClassificationsReturnCode | String |  |
| preGenerateNodeCode | String |  |
| buildTreeCode | String |  |
| lineEndSymbol | String |  |
| buildExpFunction | String |  |
| generateCodeByClassificationsNum | String |  |
| findReplaceIds | List<String> |  |
| buildMultipleClassificationsResultLogicCode | String |  |
| generateTreeSum | String |  |
| build2ClassificationsResultLogicCode | String |  |
| generateTreeClassificationsResultSum | String |  |
| treeMultipleClassificationsModMap | Map<Integer, List<String>> |  |
| preBuildMultipleClassificationsMethodSignNameCode | String |  |
| indentationNum | String |  |
| preGenerateTreeNodeCode | void |  |
| generateTreeSum | String |  |
| greaterThanSymbol | String |  |
| generateVarDef | String |  |
| generateCompareVarName | String |  |




