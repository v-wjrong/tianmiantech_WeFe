# 基础信息

|      |      |
|------|------|
| 名称 | common-verification-code |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-verification-code |
| 包名 | docs.common.java.common-verification-code |
| 概述说明 | 阿里云短信服务Java客户端，封装SDK提供短信发送功能，支持验证码场景，依赖阿里云SDK。邮件发送模块封装SMTP协议，支持HTML邮件和SSL加密，依赖JavaMail。验证码管理模块定义业务类型和发送渠道枚举，无外部依赖。抽象验证码服务类提供生成、发送和校验功能，有效期2分钟。工厂类根据渠道返回短信或邮件客户端实例。抽象客户端和响应类提供基础封装，需子类实现具体逻辑。 |

# 说明

## 概述  
该模块是统一验证码服务框架，核心职责是提供多通道（短信/邮件）验证码的标准化管理，涵盖生成、发送和校验全流程。接口规范包含抽象客户端（AbstractClient）和响应基类（AbstractResponse），采用工厂模式（ClientFactory）动态选择发送渠道。关键数据结构包括验证码业务枚举（VerificationCodeBusinessType）、渠道枚举（CaptchaSendChannel）和扩展参数映射。外部依赖为阿里云短信SDK和JavaMail库。例如通过ExpiringMap实现2分钟有效期的验证码缓存。

## 主要业务场景  
典型流程为：选择业务类型（如会员注册）→指定发送渠道（短信/邮件）→工厂获取对应客户端→发送并校验验证码。交互模式类似网关路由，通过状态码（如RESP_STATUS_OK）判断结果。功能完整性体现在多通道支持、缓存管理和异常处理，例如短信发送使用AliyunSmsClient，邮件发送依赖JavaMailSender。集成案例包括用户注册时的短信验证码下发和密码找回的邮件通知。


### 包内部结构视图

None

# 文件列表

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | 阿里云短信服务Java客户端，封装SDK提供短信发送功能，支持验证码场景，依赖阿里云SDK。邮件发送模块封装SMTP协议，支持HTML邮件和SSL加密，依赖JavaMail。验证码管理模块定义业务类型和发送渠道枚举，无外部依赖。抽象验证码服务类提供生成、发送和校验功能，有效期2分钟。工厂类根据渠道返回短信或邮件客户端实例。抽象客户端和响应类提供基础封装，需子类实现具体逻辑。 |


