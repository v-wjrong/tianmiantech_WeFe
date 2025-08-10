# 基础信息

|      |      |
|------|------|
| 名称 | common |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-web/src/main/java/com/welab/wefe/common |
| 包名 | docs.common.java.common-web.src.main.java.com.welab.wefe.common |
| 概述说明 | 该模块集成了Web API开发框架，包含日志记录、用户活动管理、权限控制、流量限制、验证码服务、文档生成等核心功能。采用注解驱动和反射机制，支持多格式文档输出和自动化校验。通过线程安全设计和防御式编程保障稳定性，适用于多角色系统和微服务场景。 |

# 说明

## 概述  
该模块是Web应用开发的全栈解决方案，核心职责包括API全生命周期管理（请求处理/权限控制/日志记录）和开发支持工具（文档生成/安全策略）。接口规范遵循分层设计，如AbstractApi基类体系、@Api注解元数据和ApiResult统一响应结构。关键数据结构涵盖日志实体（ApiLog）、权限模型（Caller枚举）、安全策略（LoginSecurityPolicy）和文档模型（ApiItem）。外部依赖包括Spring框架、SM4加密库、FastJson和并发工具类。例如通过TempRsaCache实现临时密钥管理，类似网关层的安全拦截机制。

## 主要业务场景  
模块支撑多角色系统的典型交互链：从请求入站（BaseController路由）→安全校验（LoginSecurityPolicy/RSA解密）→业务执行（ApiExecutor反射调用）→响应处理（DTO转换/日志记录）。完整功能矩阵包含：1）安全控制（如验证码服务+小黑屋机制）；2）流量治理（IP/手机号双维度限流）；3）开发辅助（API文档自动化生成）。典型集成案例表现为链式配置（Launcher初始化）、注解驱动（如@FlowLimitByMobile）和工具类组合（CurrentAccountUtil+ModelMapper），适用于中台服务快速构建。


### 包内部结构视图

```mermaid
graph TD
    common --> web
    web --> delegate
    web --> controller
    web --> api
    web --> api_document
    web --> util
    web --> service
    web --> dto
    web --> function
    web --> config
    web --> TempRsaCache.java
    web --> Launcher.java
    web --> LoginSecurityPolicy.java
    web --> ApiExecutor.java
    delegate --> api_log
    api_log --> ApiLog.java
    api_log --> ApiCallerType.java
    api_log --> AbstractApiLogger.java
    controller --> BaseController.java
    api --> dev
    api --> base
    api --> LogoutApi.java
    dev --> Apis.java
    dev --> ErrorSqlList.java
    dev --> EnvApi.java
    dev --> DownloadLogFile.java
    dev --> SlowSqlList.java
    dev --> FindLogFileException.java
    dev --> HttpBinApi.java
    dev --> CreateTestDataSetApi.java
    base --> Caller.java
    base --> FlowLimitByMobile.java
    base --> FlowLimitByIp.java
    base --> Api.java
    base --> AbstractNoneOutputApi.java
    base --> AbstractApi.java
    base --> AbstractNoneInputApi.java
    api_document --> model
    api_document --> MarkdownFormatter.java
    api_document --> AbstractApiDocumentFormatter.java
    api_document --> JsonFormatter.java
    api_document --> HtmlFormatter.java
    model --> ApiItem.java
    model --> ApiParamField.java
    model --> ApiParam.java
    util --> DatabaseEncryptConverter.java
    util --> HttpServletRequestUtil.java
    util --> DatabaseEncryptUtil.java
    util --> CurrentAccountUtil.java
    util --> ModelMapper.java
    service --> account
    service --> flowlimit
    service --> CaptchaService.java
    account --> HistoryPasswordItem.java
    account --> SsoAccountInfo.java
    account --> AccountInfo.java
    flowlimit --> AbstractMemoryFlowLimitService.java
    flowlimit --> FlowLimitByIpService.java
    flowlimit --> AbstractFlowLimitService.java
    flowlimit --> FlowLimitByMobileService.java
    dto --> AbstractWithFilesApiInput.java
    dto --> AbstractTimedApiOutput.java
    dto --> GatewayMemberInfo.java
    dto --> Captcha.java
    dto --> NoneApiOutput.java
    dto --> UploadFileApiOutput.java
    dto --> PageableApiInput.java
    dto --> ApiResult.java
    dto --> UniqueIDApiInput.java
    dto --> AbstractApiOutput.java
    dto --> AbstractApiInput.java
    dto --> NoneApiInput.java
    dto --> PageableApiOutput.java
    dto --> AbstractSecureBoostInput.java
    dto --> AbstractLRInput.java
    dto --> AbstractGridSearchParam.java
    dto --> SignedApiInput.java
    function --> FlowLimitByMobileFunction.java
    function --> CheckSessionTokenFunction.java
    function --> BeforeApiExecuteFunction.java
    function --> AfterApiExecuteFunction.java
    function --> ApiPermissionPolicyFunction.java
    function --> OnApiExceptionFunction.java
    function --> FlowLimitByIpFunction.java
    config --> AppConfig.java
    config --> ApiBeanNameGenerator.java
    config --> MyCorsFilter.java
    config --> CommonConfig.java
```

该流程图展示了WeFe项目中common-web模块的完整目录结构，从根目录common开始，逐级展开web子目录及其所有子模块。图中清晰呈现了controller、api、service等核心模块的层级关系，以及各模块下的具体文件分布，特别是api模块下dev和base子模块的详细文件构成。整体结构层次分明，完整覆盖了从基础配置到业务实现的全部路径，共包含85个节点，准确反映了源代码的组织架构。

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [web](web/_module.md) | package | 该模块集成了Web API开发框架，包含日志记录、用户活动管理、权限控制、流量限制、验证码服务、文档生成等核心功能。采用注解驱动和反射机制，支持多格式文档输出和自动化校验。通过线程安全设计和防御式编程保障稳定性，适用于多角色系统和微服务场景。 |


