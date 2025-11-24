# 基础信息

|      |      |
|------|------|
| 名称 | DateUtil |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-lang/src/main/java/com/welab/wefe/common/util/DateUtil.java |
| 包名 | com.welab.wefe.common.util |
| 依赖项 | ['org.apache.commons.lang3.StringUtils', 'org.apache.commons.lang3.math.NumberUtils', 'org.apache.commons.lang3.time.DateUtils', 'org.slf4j.Logger', 'org.slf4j.LoggerFactory', 'java.math.BigInteger', 'java.text.ParseException', 'java.text.SimpleDateFormat', 'java.time.Duration', 'java.time.LocalDateTime', 'java.time.ZoneId', 'java.time.ZoneOffset', 'java.util'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DateUtil | class |  |



## 类 DateUtil

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | DateUtil |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| Y4_M2_D2_H2 = "yyyyMMddHH" | String |  |
| Y4_M2_D2_H2_M2_S2 = "yyyyMMddHHmmss" | String |  |
| LOG = LoggerFactory.getLogger(DateUtil.class) | Logger |  |
| YYYY_MM_DD_HH_MM_SS4 = "yyyy-MM-dd HH:00:00" | String |  |
| YYYYMM = "yyyyMM" | String |  |
| YYYY_MM = "yyyy-MM" | String |  |
| YYYY_MM_DD_HH = "yyyy-MM-dd HH:00:00" | String |  |
| YYYY_MM_DD_HH_MM_SS2 = "yyyy-MM-dd HH:mm:ss" | String |  |
| YYYY_MM_DDTHH_MM_SS_SSSZ = "yyyy-MM-dd'T'HH:mm:ss.SSSZ" | String |  |
| YYYY_MM_DD_HH_MM_SS3 = "yyyy-MM-dd HH:mm:00" | String |  |
| MONTH_IN_SECOND = 30 * 24 * 60 * 60 | long |  |
| YYYY_MM_DD_HH_MM = "yyyy-MM-dd HH:mm" | String |  |
| HOUR_IN_MILLIS = 60 * 60 * 1000 | long |  |
| YYYY_MM_DD = "yyyy-MM-dd" | String |  |
| DAY_IN_MILLIS = 24 * 60 * 60 * 1000 | long |  |
| YYYY_MM_DD_HH_MM_SS = "yyyy-MM-dd.HH.mm.ss" | String |  |
| Y4_M2_D2 = "yyyyMMdd" | String |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| intervalDaysUntilNow | Long |  |
| addMonths | Date |  |
| getCurrentDate3 | String |  |
| getCurrentDate2 | String |  |
| isDatePattern | boolean |  |
| intervalMonths | long |  |
| getCurrentDate | String |  |
| addMinutes | Date |  |
| toString | String |  |
| addMonth | String |  |
| getTimeFromtFormat | long |  |
| stringToDate | Date |  |
| getLastDay | Date |  |
| toStringYYYY_MM_DD_HH_MM_SS2 | String |  |
| getTimestamp | long |  |
| getAfterDay | Date |  |
| getNextDay | Date |  |
| isEffectiveDate | boolean |  |
| getCurrentTimeStr | String |  |
| getEveryMonths | List<String> |  |
| getTimeLong | long |  |
| stringToTimeInMillis | long |  |
| toStringYYYY_MM_DDTHH_MM_SS_SSSZ | String |  |
| getEverydays | List<String> |  |
| getTimeFromtFormat2 | long |  |
| currentDateMillis | long |  |
| spend2PrettyText | String |  |
| getAfterMonthFirstDay | Date |  |
| minusDays | Date |  |
| localToUtc | Date |  |
| daysBetween | int |  |
| isWithinSpecifiedTime4Month | boolean |  |
| isWithinSpecifiedTime | boolean |  |
| getLastMonthFirstDay | Date |  |
| getCurrentDay | Date |  |
| intervalDaysUntilNow | Long |  |
| timeInMillisToDate | String |  |
| addYears | Date |  |
| dateMillis | long |  |
| addDays | Date |  |
| intervalDays | Long |  |
| getDate | Date |  |
| dateToTimeInMillis | long |  |
| convertMillisecond | long |  |
| getFirstSecondOfMonth | long |  |
| intervalSeconds | Long |  |
| timeInMillisToDate | String |  |
| convertSecond | long |  |
| getFirstSecondOfMonthString | String |  |
| intervalDays | Long |  |
| getDay | int |  |
| convertSecond | long |  |
| formatStringDate | String |  |
| addHours | Date |  |
| fromString | Date |  |
| getHour | int |  |
| monthsBetween | int |  |
| intervalDays | Long |  |
| getNextMonthFirstDay | Date |  |
| toStringYYYY_MM_DD | String |  |
| dateBetween | boolean |  |
| formatDate | Date |  |
| intervalMonths | int |  |
| getDateBeforeMonth | String |  |
| hexStrToDate | Date |  |




