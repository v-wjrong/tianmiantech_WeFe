# Basic Information

|      |      |
|------|------|
| Name | common-web |
| Language | .java |
| Code Path | WeFe/common/java/common-web |
| Package Name | docs.common.java.common-web |
| Brief Description | This module integrates a Web API development framework, encompassing core functionalities such as logging, user activity management, permission control, traffic limiting, CAPTCHA services, and documentation generation. It adopts an annotation-driven approach and reflection mechanism, supporting multi-format document output and automated validation. With thread-safe design and defensive programming to ensure stability, it is suitable for multi-role systems and microservices scenarios. |

# Description

## Overview  
This module serves as a full-stack solution for web application development, with core responsibilities encompassing API lifecycle management (request handling/authorization control/logging) and development support tools (documentation generation/security policies). The interface specification adheres to a layered design, including the AbstractApi base class system, @Api annotation metadata, and the ApiResult unified response structure. Key data structures cover log entities (ApiLog), permission models (Caller enum), security policies (LoginSecurityPolicy), and documentation models (ApiItem). External dependencies include the Spring framework, SM4 encryption library, FastJson, and concurrency utility classes. For example, temporary key management is implemented via TempRsaCache, resembling the security interception mechanism at the gateway layer.  

## Core Business Scenarios  
The module supports typical interaction chains in multi-role systems: from inbound requests (BaseController routing) → security validation (LoginSecurityPolicy/RSA decryption) → business execution (ApiExecutor reflective invocation) → response processing (DTO conversion/logging). The complete functional matrix includes: 1) Security controls (e.g., captcha service + blacklist mechanism); 2) Traffic governance (dual-dimensional rate limiting by IP/mobile number); 3) Development assistance (automated API documentation generation). Typical integration cases manifest as chained configurations (Launcher initialization), annotation-driven approaches (e.g., @FlowLimitByMobile), and utility class combinations (CurrentAccountUtil + ModelMapper), making it suitable for rapid mid-platform service construction.


### Package Internal Structure View

None

# File List

| Name   | Type  | Description |
|-------|------|-------------|
| [com](src/main/java/com/_module.md) | folder | This module integrates a Web API development framework, encompassing core functionalities such as logging, user activity management, permission control, traffic limiting, CAPTCHA services, and documentation generation. It adopts an annotation-driven approach and reflection mechanism, supporting multi-format document output and automated validation. With thread-safe design and defensive programming to ensure stability, it is suitable for multi-role systems and microservices scenarios. |


