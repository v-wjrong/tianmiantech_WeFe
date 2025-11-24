# Basic Information

|      |      |
|------|------|
| Name | TextFileIterator |
| Language | .java |
| Code Path | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/io/text/reader/TextFileIterator.java |
| Package Name | com.welab.wefe.common.io.text.reader |
| Dependencies | ['org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.BufferedReader', 'java.io.Closeable', 'java.io.IOException', 'java.util.Iterator'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| TextFileIterator | class |  |



## Class TextFileIterator

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | TextFileIterator |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| reader | AbstractTextReader |  |
| lastLine = false | boolean |  |
| logger = LoggerFactory.getLogger(this.getClass()) | Logger |  |
| hasNext = true | boolean |  |
| currentLineIndex = -1 | long |  |
| currentLine | String |  |
| bufferedReader | BufferedReader |  |

### Method List

| Name  | Type  | Description |
|-------|-------|------|
| next | String |  |
| hasNext | boolean |  |
| readLine | void |  |
| remove | void |  |
| getCurrentLineIndex | long |  |
| close | void |  |




