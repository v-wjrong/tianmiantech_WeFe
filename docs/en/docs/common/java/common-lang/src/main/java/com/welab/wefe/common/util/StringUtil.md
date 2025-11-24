# Basic Information

|      |      |
|------|------|
| Name | StringUtil |
| Language | .java |
| Code Path | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/util/StringUtil.java |
| Package Name | com.welab.wefe.common.util |
| Dependencies | ['com.welab.wefe.common.function.CharFunction', 'org.apache.commons.lang3.StringUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.io.UnsupportedEncodingException', 'java.nio.charset.StandardCharsets', 'java.security.MessageDigest', 'java.util.ArrayList', 'java.util.List', 'java.util.Map', 'java.util.regex.Matcher', 'java.util.regex.Pattern'] |
| Brief Description |  |

# Description



# Class Summary

| Name   | Type  | Description |
|-------|------|-------------|
| StringUtil | class |  |



## Class StringUtil

|      |      |
|------|------|
| Access Modifier | public |
| Type | class |
| Name | StringUtil |
| Description |  |


### UML Class Diagram




### Internal Method Call Graph



### Field List

| Name  | Type  | Description |
|-------|-------|------|
| PATTERN_MATCH_CHINESE_CHARACTER = Pattern.compile("[\\u4e00-\\u9fa5]") | Pattern |  |
| MATCH_PHONENUMBER = Pattern.compile("^((\\+86)|(86))?1[3456789]\\d{9}$") | Pattern |  |
| PATTERN_MATCH_UNDERLINE_CHARACTER = Pattern.compile("_(\\w)") | Pattern |  |
| LOG = LoggerFactory.getLogger(StringUtil.class) | Logger |  |

### Method List

| Name  | Type  | Description |
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




