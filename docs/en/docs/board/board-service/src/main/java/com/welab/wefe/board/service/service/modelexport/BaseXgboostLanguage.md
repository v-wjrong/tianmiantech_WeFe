# Basic Information

|      |      |
|------|------|
| Name | BaseXgboostLanguage |
| Language | .java |
| Code Path | WeFe/board/board-service/src/main/java/com/welab/wefe/board/service/service/modelexport/BaseXgboostLanguage.java |
| Package Name | com.welab.wefe.board.service.service.modelexport |
| Dependencies | ['com.welab.wefe.common.util.JObject', 'org.apache.commons.collections4.CollectionUtils', 'java.util.ArrayList', 'java.util.LinkedHashMap', 'java.util.List', 'java.util.Map', 'java.util.regex.Matcher', 'java.util.regex.Pattern'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| BaseXgboostLanguage | class |  |



## Class BaseXgboostLanguage

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | BaseXgboostLanguage |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| INDENTATION_UNIT_CHAR = "    " | String |  |
| MAX_LOOP_COUNT = 1000 | int |  |
| ROOT_NODE_KEY = "0" | String |  |
| SPECIAL_NUMERIC = "#" | String |  |
| METHOD_BODY_PLACEHOLDER = "#body#" | String |  |
| NUM_CLASSES_2_CLASSIFICATIONS = 2 | int |  |

### Method List

| Name  | Type  | Description |
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




