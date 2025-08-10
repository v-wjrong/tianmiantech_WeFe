
# WeFe

## Overview  
This project is a full-stack platform in the field of federated learning and privacy-preserving computation, positioned as a "distributed AI infrastructure for secure multi-party collaboration," akin to an encrypted AI collaboration factory. It primarily addresses the challenge of joint modeling in data silo scenarios, achieving "data availability without visibility" through multi-layer security protocols (e.g., PSI/PIR/SA), catering to cross-institutional data collaboration scenarios such as financial risk control and medical research.  

The architecture adopts a microservices layered design, integrating the gateway layer (gRPC communication), computation layer (MPC algorithms), management layer (blockchain RBAC), and storage layer (multi-database adaptation). Core resources include: 1) SDK toolchain (e.g., PSI client/certificate manager); 2) CLI management console; 3) smart contract components. The tech stack combines the Spring ecosystem, national cryptographic algorithms, FISCO BCOS consortium blockchain, and machine learning frameworks (XGBoost/PaddlePaddle), forming an end-to-end workflow from data alignment → joint training → secure prediction.  

## What is WeFe?  
WeFe is a modular federated learning operating system, with core functionalities including: 1) **Secure Data Alignment** (encrypted sample matching based on RSA-PSI protocol, akin to a blind signature process); 2) **Joint Modeling** (merging gradients via distributed XGBoost, resembling a privacy-enhanced version of MapReduce); 3) **Blockchain Governance** (smart contract-managed member onboarding, similar to a decentralized ticketing system).  

The technical implementation relies on a three-tier architecture: infrastructure layer (gateway/certificate services), algorithm layer (MPC protocol stack), and application layer (RESTful API). A typical workflow involves Medical Institution A encrypting data via the gateway → performing PSI alignment with Institution B → jointly training a logistic regression model → returning results after blockchain auditing. Module interactions employ an "event-driven + factory pattern," such as certificate issuance triggering smart contract events and ClientFactory dynamically loading CAPTCHA services.  

Application scenario templates include: 1) **Cross-Bank Anti-Fraud** (PSI-matched blacklists → secure aggregated models); 2) **Medical Research** (PIR-retrieved case records → federated learning modeling); 3) **Government Data Openness** (blockchain-based permission control → multi-party computation statistics). Key implementations include ensuring communication security via the SM2 national cryptographic algorithm, accelerating data deduplication with BloomFilterUtils, and enabling gRPC streaming fragment transmission through GatewayMetaProto, forming end-to-end privacy protection from data to services.

## Quick Navigation

### 💻 Developers

- [Development Guide](summary/dev_guide.md) - Quickly get started with project development


- [Module Description](docs/_module.md) - Detailed explanation of project modules


### 🏗️ Architect

- [System Architecture](summary/system_architecture.md) - System Architecture


### ↔️ API Documentation

- <a href='https://code2docs.ai/wiki/tianmiantech/WeFe/72cc75175615b41ee1c754dcc0a704553d6478b7/api-viewer.html' target='_blank'>API Documentation</a> - API Documentation

