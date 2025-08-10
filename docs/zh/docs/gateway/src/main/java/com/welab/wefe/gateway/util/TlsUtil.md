# 基础信息

|      |      |
|------|------|
| 名称 | TlsUtil |
| 编码语言 | .java |
| 代码路径 | WeFe/gateway/src/main/java/com/welab/wefe/gateway/util/TlsUtil.java |
| 包名 | com.welab.wefe.gateway.util |
| 依赖项 | ['com.webank.cert.toolkit.utils.CertUtils', 'com.welab.wefe.gateway.cache.CaCertificateCache', 'org.apache.commons.collections4.CollectionUtils', 'java.security.cert.X509Certificate', 'java.util.List'] |
| 概述说明 | TlsUtil类提供两个静态方法：buildCertificates将CA证书列表转为X509Certificate数组，getAllCertificates根据tlsEnable标志返回全部证书或null。 |

# 说明

TlsUtil类包含两个静态方法用于处理X509证书。buildCertificates方法接收CA证书列表，若列表为空则返回null，否则将每个证书内容转换为X509Certificate对象并存入数组返回。getAllCertificates方法根据tlsEnable参数决定是否调用buildCertificates，若启用则从CaCertificateCache获取全部证书并转换，否则返回null。两个方法都可能抛出异常。

# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| TlsUtil | class | TlsUtil类提供两个静态方法：buildCertificates将CA证书列表转为X509Certificate数组，若列表为空返回null；getAllCertificates根据tlsEnable参数决定是否获取全部CA证书并转换。 |



## 类 TlsUtil

|      |      |
|------|------|
| 访问范围 | public |
| 类型 | class |
| 名称 | TlsUtil |
| 说明 | TlsUtil类提供两个静态方法：buildCertificates将CA证书列表转为X509Certificate数组，若列表为空返回null；getAllCertificates根据tlsEnable参数决定是否获取全部CA证书并转换。 |


### UML类图

```mermaid
classDiagram
    class TlsUtil {
        <<Utility>>
        +X509Certificate[] buildCertificates(List~CaCertificateCache.CaCertificate~ caCertificateList) throws Exception
        +X509Certificate[] getAllCertificates(boolean tlsEnable) throws Exception
    }

    class CaCertificateCache {
        <<Singleton>>
        +List~CaCertificate~ getAll()
        +CaCertificateCache getInstance()
    }

    class CaCertificate {
        -String content
        +String getContent()
    }

    class CertUtils {
        <<Utility>>
        +X509Certificate convertStrToCert(String content)
    }

    TlsUtil --> CaCertificateCache : 依赖
    TlsUtil --> CertUtils : 依赖
    CaCertificateCache --> CaCertificate : 包含
```

该代码展示了一个TLS工具类TlsUtil，用于构建X509证书数组。它依赖CaCertificateCache单例类获取CA证书列表，并通过CertUtils工具类将字符串转换为证书对象。CaCertificateCache包含内部类CaCertificate存储证书内容。整体设计遵循工具类模式，提供静态方法处理证书转换逻辑，支持根据TLS开关条件获取所有证书。


### 内部方法调用关系图

```mermaid
graph TD
    A["类TlsUtil"]
    B["静态方法: buildCertificates(List<CaCertificateCache.CaCertificate> caCertificateList)"]
    C["检查: CollectionUtils.isEmpty(caCertificateList)"]
    D["返回: null"]
    E["创建数组: X509Certificate[caCertificateList.size()]"]
    F["循环: for (int i = 0; i < caCertificateList.size(); i++)"]
    G["获取证书: CaCertificateCache.CaCertificate c = caCertificateList.get(i)"]
    H["转换证书: CertUtils.convertStrToCert(c.getContent())"]
    I["存入数组: certificates[i] = cert"]
    J["返回: certificates"]
    K["静态方法: getAllCertificates(boolean tlsEnable)"]
    L["条件判断: tlsEnable ?"]
    M["调用: CaCertificateCache.getInstance().getAll()"]
    N["调用: buildCertificates()"]
    O["返回: null"]

    A --> B
    B --> C
    C --"是"--> D
    C --"否"--> E
    E --> F
    F --> G
    G --> H
    H --> I
    I --> F
    F --"循环结束"--> J
    A --> K
    K --> L
    L --"是"--> M
    M --> N
    N --> B
    L --"否"--> O
```

该流程图展示了TlsUtil类的两个核心方法逻辑。buildCertificates方法首先检查输入列表是否为空，若为空则返回null，否则遍历列表将每个证书内容转换为X509Certificate对象并存入数组。getAllCertificates方法根据tlsEnable标志决定是否获取并构建证书数组，体现了条件分支和内部方法调用的完整流程。

### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| buildCertificates | X509Certificate[] | 方法将CA证书列表转换为X509Certificate数组，若列表为空返回null。遍历列表，使用CertUtils将证书内容转为X509Certificate对象并存入数组。 |
| getAllCertificates | X509Certificate[] | 该方法根据tlsEnable参数决定返回所有TLS证书数组或null。若启用TLS，则从CaCertificateCache获取证书并构建数组；否则返回空值。 |




