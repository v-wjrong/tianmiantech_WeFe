# Basic Information

|      |      |
|------|------|
| Name | com |
| Language | .java |
| Code Path | WeFe/common/java/common-lang/src/main/java/com |
| Package Name | docs.common.java.common-lang.src.main.java.com |
| Brief Description | Java configuration management toolset, uniformly manages configurations and provides type-safe interfaces. Supports multi-environment configuration loading and type conversion, dependent on Log4j. Data processing toolset includes Excel parsing and text batch processing, supporting ETL and log analysis. Field validation platform implements sensitive data masking and format validation. The basic constants module defines key types and compression formats. General utility library covers encryption, collection operations, etc. HTTP communication module manages file downloads and request handling. Compression/decompression module supports multi-format processing. Functional interfaces support Lambda operations. Thread pool management tool provides task execution functionality. Validation classes check data type legality. Status code enumeration defines system error codes. Security tools generate random salt values. Time interval class handles time calculations. Batch consumer class implements batch data processing. Captcha generation class creates Base64 captchas. Information size class converts storage units. Data type conversion class handles multi-format conversions. Sampling log class controls log frequency. Timing utility class records code execution time. |

# Description

## Overview  
This module is a comprehensive library of Java foundational utilities and functional components, with core responsibilities including configuration management, data processing, field validation, HTTP communication, and other basic service support. It adopts a static utility class design pattern, providing type-safe interfaces and functional programming support. Key data structures include CompositeConfiguration (composite configuration), Excel worksheets/cells, regular expression rule libraries, and enumerated constants. External dependencies include Log4j, Apache HttpClient, BouncyCastle, etc. For example, the configuration module relies on Log4j, while the encryption module uses BouncyCastle to implement national cryptographic algorithms.  

The module integrates functionalities across multiple domains, resembling infrastructure middleware. For instance, the Configurations class manages multi-environment configurations, ExcelReader provides lightweight encapsulation of POI operations, and FieldValidateUtil handles sensitive data masking. Technical features include annotation-driven mechanisms (e.g., @Check), strategy enumerations (e.g., SecretKeyType), and stream processing (e.g., BatchConsumer). All components adhere to the "out-of-the-box" principle, such as SecurityUtil generating encryption salts and TimeSpan handling time interval calculations.  

## Key Business Scenarios  
Typical applications form three major closed loops: 1) **Configuration and Security Loop**: Loading configurations via ConfigurationManager → validating with FieldValidateUtil → encrypting with SecurityUtil, such as reading database connection parameters and validating sensitive fields; 2) **Data Processing Loop**: Combining ExcelReader parsing → BatchConsumer batch processing → File compression storage, resembling an ETL pipeline; 3) **Communication and Scheduling Loop**: HttpClient API calls → CommonThreadPool asynchronous execution → Stopwatch performance monitoring.  

The unified interaction mode combines chained calls with annotation-driven mechanisms. For example, the Excel module follows a "load-iterate-close" workflow, while the validation module triggers rules via the @Check annotation. Functional completeness is reflected in coverage of national cryptographic algorithms (SM2/SM4), multi-protocol support (HTTP/ZIP), and full lifecycle management (e.g., configuration loading → usage → monitoring). Typical scenarios include: financial-grade data validation (ID cards/phone numbers), high-concurrency file processing (chunked compression/downloads), and secure communication (HTTPS + signature verification). For instance, HttpRequest automatically handles 302 redirects, and Validator verifies date-time formats.


### Package Internal Structure View

```mermaid
graph TD
    com --> welab
    welab --> wefe
    wefe --> common
    common --> configuration
    common --> fastjson
    common --> enums
    common --> io
    common --> fieldvalidate
    common --> constant
    common --> util
    common --> exception
    common --> http
    common --> file
    common --> function
    common --> CommonThreadPool.java
    common --> Validator.java
    common --> StatusCode.java
    common --> SecurityUtil.java
    common --> TimeSpan.java
    common --> BatchConsumer.java
    common --> WeSpecCaptcha.java
    common --> InformationSize.java
    common --> Convert.java
    common --> SamplingLogger.java
    common --> Stopwatch.java
    configuration --> Configurations.java
    configuration --> ConfigurationManager.java
    fastjson --> LoggerValueFilter.java
    enums --> FilePublicLevel.java
    io --> excel
    io --> text
    excel --> ExcelReader.java
    text --> writer
    text --> reader
    writer --> delegate
    writer --> LocalTextFileWriter.java
    writer --> AbstractTextWriter.java
    delegate --> RecordToStringFunction.java
    delegate --> FileNameFunction.java
    reader --> TextFileIterator.java
    reader --> LocalTextFileReader.java
    reader --> AbstractTextReader.java
    fieldvalidate --> secret
    fieldvalidate --> annotation
    fieldvalidate --> StandardFieldType.java
    fieldvalidate --> FieldValidateUtil.java
    fieldvalidate --> FieldAssert.java
    fieldvalidate --> ReactionaryKeywords.java
    fieldvalidate --> AbstractCheckModel.java
    secret --> SecretValueFilter.java
    secret --> SecretUtil.java
    secret --> Secret.java
    secret --> MaskStrategy.java
    annotation --> Check.java
    constant --> SecretKeyType.java
    constant --> ZipType.java
    constant --> Constant.java
    util --> enums
    util --> MapUtil.java
    util --> ReflectionsUtil.java
    util --> IpAddressUtil.java
    util --> Sha1.java
    util --> ListUtil.java
    util --> StringUtil.java
    util --> EncryptUtils.java
    util --> SignUtil.java
    util --> UrlUtil.java
    util --> DateUtil.java
    util --> SM2Util.java
    util --> SM4Util.java
    util --> ClassUtils.java
    util --> JObject.java
    util --> Masker.java
    util --> OS.java
    util --> Base64Util.java
    util --> ZipUtil.java
    util --> Md5.java
    util --> ImageUtil.java
    util --> FileUtil.java
    util --> XmlUtil.java
    util --> CommentedProperties.java
    util --> AESUtil.java
    util --> RandomUtil.java
    util --> FileType.java
    util --> ThreadUtil.java
    util --> CopyUtil.java
    util --> GzipUtil.java
    util --> HostUtil.java
    util --> AsymmetricCryptoUtil.java
    util --> RSAUtil.java
    enums --> ContentType.java
    exception --> StatusCodeWithException.java
    http --> download
    http --> MyRedirectStrategy.java
    http --> HttpContentType.java
    http --> HttpMethod.java
    http --> HttpResponse.java
    http --> HttpRequest.java
    download --> DownloadResult.java
    download --> HttpDownloader.java
    download --> DownloadStatus.java
    file --> compression
    file --> decompression
    compression --> impl
    compression --> CompressionType.java
    compression --> AbstractCompression.java
    impl --> Zip.java
    impl --> Tgz.java
    decompression --> impl
    decompression --> dto
    decompression --> SuperDecompressor.java
    decompression --> AbstractDecompression.java
    impl --> Zip.java
    impl --> SevenZip.java
    impl --> Tgz.java
    dto --> DecompressionResult.java
    function --> CharFunction.java
    function --> ConsumerWithException.java
    function --> ToBooleanFunction.java
```

This flowchart presents the complete directory structure of the common-lang module in the WeFe project, starting from the top-level com package and hierarchically expanding to include major submodules such as configuration, fastjson, enums, and their internal files. The diagram clearly illustrates containment relationships at each level, including the excel and text submodules under the io module, as well as the writer and reader components within the text module. The entire structure comprises over 100 nodes, fully reflecting the organizational approach of core functionalities like utility classes, enumerations, and exception handling in the project.

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [welab](welab/_module.md) | package | Java Configuration Management Toolset, which uniformly manages configurations and provides type-safe interfaces. Supports multi-environment configuration loading and type conversion, dependent on Log4j. The data processing toolset includes Excel parsing and text batch processing, supporting ETL and log analysis. The field validation platform implements sensitive data masking and format validation. The basic constants module defines key types and compression formats. The general utility library covers encryption, collection operations, and more. The HTTP communication module manages file downloads and request processing. The compression/decompression module supports multi-format processing. Functional interfaces support Lambda operations. The thread pool management tool provides task execution functionality. The validation class checks data type legality. The status code enumeration defines system error codes. The security tool generates random salt values. The time interval class handles time calculations. The batch consumer class implements batch data processing. The captcha generation class creates Base64 captchas. The information size class converts storage units. The data type conversion class handles multi-format conversions. The sampling log class controls log frequency. The timing utility class records code execution time. |


