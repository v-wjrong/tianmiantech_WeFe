# 基础信息

|      |      |
|------|------|
| 名称 | StringUtil |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/util/StringUtil.java |
| 包名 | com.welab.wefe.common.util |
| 依赖项 | ['com.welab.wefe.common.function.CharFunction', 'org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.UnsupportedEncodingException', 'java.nio.charset.StandardCharsets', 'java.security.MessageDigest', 'java.util.ArrayList', 'java.util.List', 'java.util.Map', 'java.util.regex.Matcher', 'java.util.regex.Pattern'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| StringUtil | class |  |



## 类 StringUtil

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | StringUtil |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| PATTERN_MATCH_CHINESE_CHARACTER = Pattern.compile("[\\u4e00-\\u9fa5]") | Pattern |  |
| MATCH_PHONENUMBER = Pattern.compile("^((\\+86)|(86))?1[3456789]\\d{9}$") | Pattern |  |
| PATTERN_MATCH_UNDERLINE_CHARACTER = Pattern.compile("_(\\w)") | Pattern |  |
| LOG = LoggerFactory.getLogger(StringUtil.class) | Logger |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| substringByByteLength | String |  |
| substringRightLength | String |  |
| isEmptyToBlank | String |  |
| ToDbc | String |  |
| substringByByteLength | String |  |
| splitWithoutEmptyItem | List<String> |  |
| trim | String |  |
| strTrim | String |  |
| checkPhoneNumber | boolean |  |
| isChineseCharacter | boolean |  |
| equalsIgnoreMask | boolean |  |
| joinByComma | String |  |
| underLineCaseToCamelCase | String |  |
| camelCaseToUnderLineCase | String |  |
| parserMapStringEmptyValueAsNull | Map<String, Object> |  |
| stringToUnderLineLowerCase | String |  |
| strTrim2 | String |  |
| md5 | String |  |




