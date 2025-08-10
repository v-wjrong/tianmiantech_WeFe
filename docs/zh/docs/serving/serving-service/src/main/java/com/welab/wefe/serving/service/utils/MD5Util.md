# 基础信息

|      |      |
|------|------|
| 名称 | MD5Util |
| 编码语言 | .java |
| 代码路径 | WeFe/serving/serving-service/src/main/java/com/welab/wefe/serving/service/utils/MD5Util.java |
| 包名 | com.welab.wefe.serving.service.utils |
| 依赖项 | ['java.security.MessageDigest'] |
| 概述说明 | MD5Util类提供MD5加密功能，包含getMD5String方法进行字符串加密和byte2Hex方法将字节转为16进制字符串。 |

# 说明

这是一个名为MD5Util的Java工具类，提供MD5加密功能。类中包含两个方法：getMD5String方法接收字符串参数，使用Java原生MessageDigest类实现MD5加密，处理过程中指定UTF-8编码，并通过byte2Hex方法将结果转为16进制字符串返回；byte2Hex是私有方法，将字节数组转换为16进制字符串表示，确保每个字节转换为两位16进制数，不足位时补零。异常情况下会打印堆栈信息但不会中断程序执行。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| MD5Util | class | MD5Util类提供MD5加密功能，包含getMD5String方法进行UTF-8编码的MD5加密，以及byte2Hex私有方法将byte数组转为16进制字符串。 |



## 类 MD5Util

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | MD5Util |
| 说明 | MD5Util类提供MD5加密功能，包含getMD5String方法进行UTF-8编码的MD5加密，以及byte2Hex私有方法将byte数组转为16进制字符串。 |


### UML类图

```mermaid
classDiagram
    class MD5Util {
        <<工具类>>
        +String getMD5String(String str)
        -String byte2Hex(byte[] bytes)
    }
```

```mermaid
flowchart TD
    A["开始"] --> B["输入字符串str"]
    B --> C["获取MessageDigest实例"]
    C --> D["更新digest为UTF-8字节"]
    D --> E["调用digest生成哈希字节数组"]
    E --> F["调用byte2Hex转换为16进制"]
    F --> G["返回加密结果"]
    G --> H["结束"]

    subgraph byte2Hex流程
        F --> I["初始化StringBuilder"]
        I --> J["遍历字节数组"]
        J --> K["字节转16进制字符串"]
        K --> L{"长度是否为1?"}
        L -- 是 --> M["补0操作"]
        L -- 否 --> N["直接追加"]
        M --> N
        N --> O["返回拼接结果"]
    end
```

该代码实现了一个MD5加密工具类，核心功能是将输入字符串通过MessageDigest进行MD5哈希计算，再将生成的字节数组转换为16进制字符串表示。类图显示这是一个无状态的工具类，包含公开的加密方法和私有的字节转换方法。流程图详细描述了主加密流程和字节转换子流程，其中特别注意了单字符十六进制值的补零处理，确保输出格式的统一性。整个设计符合工具类的典型特征，具有单一职责和静态方法调用特性。


### 内部方法调用关系图

```mermaid
graph TD
    A["类MD5Util"]
    B["公开方法: getMD5String(String str)"]
    C["私有方法: byte2Hex(byte[] bytes)"]
    D["异常处理: catch(Exception e)"]
    E["调用: MessageDigest.getInstance('MD5')"]
    F["调用: str.getBytes('UTF-8')"]
    G["调用: messageDigest.update()"]
    H["调用: messageDigest.digest()"]
    I["调用: byte2Hex()"]
    J["循环处理每个byte"]
    K["调用: Integer.toHexString()"]
    L["补零操作: sb.append('0')"]
    M["返回结果: sb.toString()"]

    A --> B
    A --> C
    B --> E
    B --> F
    B --> G
    B --> H
    B --> I
    B --> D
    I --> C
    C --> J
    J --> K
    K -->|长度=1| L
    K -->|长度>1| M
    L --> M
```

这段代码流程图展示了MD5Util工具类的核心逻辑。主流程从getMD5String方法开始，通过MessageDigest实现MD5加密，将输入字符串转为字节数组后生成哈希值，再调用byte2Hex方法将字节数组转换为16进制字符串。byte2Hex方法内部通过循环处理每个字节，使用位运算和补零操作确保输出标准的32位MD5字符串。整个过程包含异常处理机制，确保在加密失败时打印错误信息。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| byte2Hex | String | 将字节数组转换为十六进制字符串，单字节补零后拼接返回。 |
| getMD5String | String | 静态方法getMD5String接收字符串参数，使用MD5算法生成哈希值并返回十六进制字符串，异常时打印堆栈。 |




