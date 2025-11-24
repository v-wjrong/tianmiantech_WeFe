# 基础信息

|      |      |
|------|------|
| 名称 | TextFileIterator |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/io/text/reader/TextFileIterator.java |
| 包名 | com.welab.wefe.common.io.text.reader |
| 依赖项 | ['org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.BufferedReader', 'java.io.Closeable', 'java.io.IOException', 'java.util.Iterator'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TextFileIterator | class |  |



## 类 TextFileIterator

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | TextFileIterator |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| reader | AbstractTextReader |  |
| lastLine = false | boolean |  |
| logger = LoggerFactory.getLogger(this.getClass()) | Logger |  |
| hasNext = true | boolean |  |
| currentLineIndex = -1 | long |  |
| currentLine | String |  |
| bufferedReader | BufferedReader |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| next | String |  |
| hasNext | boolean |  |
| readLine | void |  |
| remove | void |  |
| getCurrentLineIndex | long |  |
| close | void |  |




