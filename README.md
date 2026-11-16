# Željko Popov — SAP BTP & Enterprise Integration Architecture Catalog

[![SAP Integration Suite](https://img.shields.io/badge/SAP%20BTP-Integration%20Suite%20(CPI%20%7C%20APIM%20%7C%20AEM%20%7C%20Edge%20%7C%20Graph)-0a6ed1?logo=sap&style=flat-square)](https://github.com/neurozeljko)
[![Architecture Governance](https://img.shields.io/badge/Methodology-SAP%20ISA--M%20%7C%20S%2F4HANA%20Clean%20Core%20%7C%20Zero--Trust-success?style=flat-square)](https://github.com/neurozeljko)
[![Engineering Rigor](https://img.shields.io/badge/QA%20%26%20GitOps-Groovy%203%20%7C%20Spock%20TDD%20%7C%20Project%20Piper%20CI%2FCD-6f42c1?style=flat-square)](https://github.com/neurozeljko)

Welcome to my **Open-Source SAP Enterprise Integration Reference Library**. This catalog contains **35 production-grade architectural blueprints** built on **SAP Business Technology Platform (SAP BTP)** and **SAP Integration Suite**, complete with exported **BPMN2 (`.iflw`) packages**, **Spock Framework TDD unit test suites** (with mocked `com.sap.gateway.ip.core.customdev.util.Message` contracts), **SAP Project Piper GitOps pipelines**, and **Architectural Decision Records (ADRs)**.

---

## 🏛️ Executive Architecture Matrix (35 Reference Blueprints)

### I. S/4HANA 2025 Master Data Governance (MDG / MDI) & EU Regulatory Mesh (Projects 31–35)
| # | Reference Repository | Architectural Pattern & Core Stack | Target ERP / Domain |
| :-: | :--- | :--- | :--- |
| **35** | [**sap-cpi-mdg-eu-vida-tax-master-governance-mesh**](https://github.com/neurozeljko/sap-cpi-mdg-eu-vida-tax-master-governance-mesh) | MDG Tax Master Governance, EU ViDA (Directive 2025/516), ISO 7064 Mod-11,10 VIES VAT & Peppol ICD | S/4HANA 2025 FPS01 (`A_BusinessPartnerTaxNumber`) |
| **34** | [**sap-cpi-mdg-csddd-eudr-supplier-traceability-mesh**](https://github.com/neurozeljko/sap-cpi-mdg-csddd-eudr-supplier-traceability-mesh) | MDG-S Supplier Governance, EU CSDDD ESG Audit, EUDR WGS84 GeoJSON Polygons & ISO 17442 LEI | S/4HANA 2025 FPS01 (`FLVN00` / `FLVN01`) |
| **33** | [**sap-cpi-mdg-financial-master-green-ledger-mesh**](https://github.com/neurozeljko/sap-cpi-mdg-financial-master-green-ledger-mesh) | MDG-F Financial Master Governance, `YCOA` Range Enforcement & SAP Green Ledger (EU CSRD / ESRS E1) | S/4HANA 2025 FPS01 (`ACDOCA` / Ledger `0L`) |
| **32** | [**sap-cpi-mdi-digital-product-passport-circular-bom**](https://github.com/neurozeljko/sap-cpi-mdi-digital-product-passport-circular-bom) | EU ESPR 2026/2027 Digital Product Passport, W3C JSON-LD VC, GS1 GTIN-14 Mod-10 & REACH SVHC Gate | S/4HANA 2025 FPS01 (`API_PRODUCT_SRV`) |
| **31** | [**sap-cpi-mdg-business-partner-golden-record-mesh**](https://github.com/neurozeljko/sap-cpi-mdg-business-partner-golden-record-mesh) | Deterministic SHA-256 Golden Record Deduplication, ISO 13616 Mod-97 IBAN Check & OFAC/EU Sanctions Gate | S/4HANA 2025 FPS01 (`API_BUSINESS_PARTNER`) |

### II. Frontier Architecture, High-Availability DR & Post-Quantum Security (Projects 26–30)
| # | Reference Repository | Architectural Pattern & Core Stack | Target ERP / Domain |
| :-: | :--- | :--- | :--- |
| **30** | [**sap-ai-core-autonomous-iflow-synthesis-swarm**](https://github.com/neurozeljko/sap-ai-core-autonomous-iflow-synthesis-swarm) | Multi-Agent Swarm on SAP AI Core, CPI Design-Time REST APIs, ISA-M Governance & Zero-Touch Piper CI/CD | SAP Ariba & S/4HANA Procurement |
| **29** | [**sap-edge-bci-neural-telemetry-data-fabric**](https://github.com/neurozeljko/sap-edge-bci-neural-telemetry-data-fabric) | SAP Edge Integration Cell DSP, HIPAA SHA-256 Anonymization, Databricks/Dataiku & SAP Graph Mesh | S/4HANA Life Sciences & Neuro-BCI |
| **28** | [**sap-cpi-pqc-quantum-safe-financial-ledger-sync**](https://github.com/neurozeljko/sap-cpi-pqc-quantum-safe-financial-ledger-sync) | BouncyCastle NIST FIPS 203 (`ML-KEM-768`) + FIPS 204 (`ML-DSA-65`) Hybrid KDF & RFC 3161 TSA | S/4HANA Advanced Financial Closing |
| **27** | [**sap-btp-s4hana-dr-active-passive-failover-mesh**](https://github.com/neurozeljko/sap-btp-s4hana-dr-active-passive-failover-mesh) | Multi-Region Active-Passive DR (`EU10 -> US10`), Anycast GSLB, AEM DMR Bridge & Global Redis Idempotency | Aerospace Satellite Telemetry & EAM |
| **26** | [**sap-cpi-pharma-coldchain-tdd-cicd**](https://github.com/neurozeljko/sap-cpi-pharma-coldchain-tdd-cicd) | Spock Framework TDD, `Message` Interface Mocking, GitHub Actions CI & SAP Project Piper (`cpiArtifactDeploy`) | Pharma GxP Cold-Chain (EU Annex 11) |

### III. API Management, Multi-iPaaS Federation & Event-Driven Mesh (Projects 15–25)
| # | Reference Repository | Architectural Pattern & Core Stack | Target ERP / Domain |
| :-: | :--- | :--- | :--- |
| **25** | [**sap-apim-open-finance-edge-gateway**](https://github.com/neurozeljko/sap-apim-open-finance-edge-gateway) | SAP API Management (APIM) Spike Arrest, Quota Enforcement & PSD3 Open Finance Monetization | Open Banking & Credit Scoring |
| **24** | [**sap-cpi-ev-charging-grid-circuit-breaker**](https://github.com/neurozeljko/sap-cpi-ev-charging-grid-circuit-breaker) | High-Throughput JMS Queue Decoupling, Deterministic Throttling & In-Flight Circuit Breaker | EV Smart Charging Grid & S/4HANA |
| **23** | [**sap-cpi-informatica-clinical-trials-datafabric**](https://github.com/neurozeljko/sap-cpi-informatica-clinical-trials-datafabric) | Informatica IICS MDM Change Data Capture (CDC), GraphQL Stitching & FDA 21 CFR Part 11 Audit | Clinical Trials & Health Cloud |
| **22** | [**sap-cpi-mulesoft-fintech-federation**](https://github.com/neurozeljko/sap-cpi-mulesoft-fintech-federation) | MuleSoft Anypoint Experience Layer to SAP CPI via mTLS 1.3, OpenTelemetry & SHA-256 Idempotency | Core Banking Omni-Channel |
| **21** | [**sap-cpi-boomi-post-merger-integration**](https://github.com/neurozeljko/sap-cpi-boomi-post-merger-integration) | Boomi AtomSphere & SAP CPI Coexistence via Strangler Fig API Facade, RSA-256 JWT & Event Mesh | M&A Post-Merger S/4HANA Sync |
| **20** | [**sap-cpi-scope3-carbon-tracking-audit**](https://github.com/neurozeljko/sap-cpi-scope3-carbon-tracking-audit) | SAP AI Core Document Extraction, SHA-256 Carbon Ledger & XSLT 3.0 EU CBAM / SEC Reporting | Scope 3 ESG Sustainability |
| **19** | [**sap-cpi-hubspot-s4hana-lead-to-cash**](https://github.com/neurozeljko/sap-cpi-hubspot-s4hana-lead-to-cash) | EOIO Distributed State Machine, HTTP 429 Rate-Limit Backoff & OData V4 Sales Order Settlement | CRM-to-S/4HANA Lead-to-Cash |
| **18** | [**sap-cpi-industry40-robotics-digitaltwin**](https://github.com/neurozeljko/sap-cpi-industry40-robotics-digitaltwin) | Persistent SCADA WebSocket Mesh, In-Memory DFS BOM Cycle Detection & Zero-Downtime JMS Fallback | Industry 4.0 Digital Twin |
| **17** | [**sap-cpi-vpp-smartgrid-carbon-trading**](https://github.com/neurozeljko/sap-cpi-vpp-smartgrid-carbon-trading) | High-Throughput Kafka Micro-Bid Aggregation, SAP MDI GraphQL Sync & OData V4 Bulk Settlement | Virtual Power Plant (VPP) |
| **16** | [**sap-cpi-v2x-fleet-predictive-maintenance**](https://github.com/neurozeljko/sap-cpi-v2x-fleet-predictive-maintenance) | Edge Integration Cell Micro-Batching, SAP AI Core Anomaly Scoring & CNCF CloudEvents 1.0 | Autonomous V2X Fleet EAM |
| **15** | [**sap-cpi-defense-aerospace-soap-aif-gateway**](https://github.com/neurozeljko/sap-cpi-defense-aerospace-soap-aif-gateway) | W3C WS-Security SOAP XI 3.0, mTLS X.509, Anti-Replay Engine & SAP AIF Fault Injection | Aerospace & Defense B2B |

### IV. S/4HANA Clean Core, B2B/B2G EDI & Legacy PI/PO Modernization (Projects 1–14)
| # | Reference Repository | Architectural Pattern & Core Stack | Target ERP / Domain |
| :-: | :--- | :--- | :--- |
| **14** | [**sap-cpi-cleancore-cap-mesh-gitops**](https://github.com/neurozeljko/sap-cpi-cleancore-cap-mesh-gitops) | Side-by-Side Node.js CAP on BTP, OAuth 2.0 RFC 8693 Token Exchange & Principal Propagation | S/4HANA Clean Core Extensions |
| **13** | [**sap-cpi-iam-payroll-zerotrust-pipeline**](https://github.com/neurozeljko/sap-cpi-iam-payroll-zerotrust-pipeline) | In-Flight FPE AES-256 Tokenization, SCIM 2.0 Provisioning & OpenPGP RSA-4096 Payroll Encryption | SuccessFactors & Banking |
| **12** | [**sap-cpi-o2c-apimesh-cleancore**](https://github.com/neurozeljko/sap-cpi-o2c-apimesh-cleancore) | APIM Edge Security, Global CSRF Token Caching, RFC 7807 Problem Details & OData V4 Clean Core | Omni-Channel Order-to-Cash |
| **11** | [**sap-cpi-oilgas-cleancore-migration**](https://github.com/neurozeljko/sap-cpi-oilgas-cleancore-migration) | Legacy SAP PI/PO SOAP-to-OData V4 Migration via SAP Cloud Connector & Principal Propagation | Oil & Gas Upstream S/4HANA |
| **10** | [**sap-cpi-greentech-ai-cleancore**](https://github.com/neurozeljko/sap-cpi-greentech-ai-cleancore) | In-Flight ML Anomaly Detection, Strangler Fig Migration & SAP AIF Error Monitoring | GreenTech Carbon Accounting |
| **09** | [**sap-cpi-globalhr-eventmesh-cleancore**](https://github.com/neurozeljko/sap-cpi-globalhr-eventmesh-cleancore) | Workday PECI Webhook Ingestion, XSLT 3.0 Canonicalization, Parallel Multicast & SAP Concur SCIM 2.0 | Global Hire-to-Retire (H2R) |
| **08** | [**sap-cpi-b2b-edifact-orders-tpm-cleancore**](https://github.com/neurozeljko/sap-cpi-b2b-edifact-orders-tpm-cleancore) | Trading Partner Management (TPM), EDIFACT D.01B `ORDERS` to `SALESORDER_CREATEFROMDAT2` IDoc & DLQ | B2B EDI Order-to-Cash |
| **07** | [**sap-cpi-procurement-gateway-cleancore-cbo**](https://github.com/neurozeljko/sap-cpi-procurement-gateway-cleancore-cbo) | SAP APIM, Ariba Open Connectors Enrichment & S/4HANA Custom Business Object (CBO) OData V4 | Procure-to-Pay Quality Gate |
| **06** | [**sap-cpi-legacy-pipo-etl-sapbuild**](https://github.com/neurozeljko/sap-cpi-legacy-pipo-etl-sapbuild) | Legacy PI/PO Migration, Groovy Data Cleansing, JDBC Ingestion & SAP Build Process Automation | Enterprise ETL & Workflow |
| **05** | [**sap-cpi-edge-kafka-event-streaming**](https://github.com/neurozeljko/sap-cpi-edge-kafka-event-streaming) | Hybrid Edge Integration Cell, High-Throughput Kafka Micro-Batching & SAP Advanced Event Mesh (AMQP) | Real-Time Retail Streaming |
| **04** | [**sap-cpi-b2g-peppol-as4-compliance**](https://github.com/neurozeljko/sap-cpi-b2g-peppol-as4-compliance) | EN16931 UBL 2.1 Transformation, ISO Schematron SVRL Validation, Peppol SML/SMP & OASIS AS4 | B2G E-Invoicing Compliance |
| **03** | [**sap-cpi-datafabric-kinaxis-mdi**](https://github.com/neurozeljko/sap-cpi-datafabric-kinaxis-mdi) | SAP Master Data Integration (MDI) Delta Sync to Kinaxis Maestro via GraphQL Cursor Pagination & DFS | Supply Chain Planning Mesh |
| **02** | [**sap-cpi-medtech-zerotrust-cleancore**](https://github.com/neurozeljko/sap-cpi-medtech-zerotrust-cleancore) | Decoupled Zero-Trust 3PL Logistics Pipeline to S/4HANA OData V4 with SHA-256 GxP Audit Hashing | MedTech 3PL Serialization |
| **01** | [**sap-cpi-gxp-desadv-delvry03**](https://github.com/neurozeljko/sap-cpi-gxp-desadv-delvry03) | GxP B2B AS2 EDIFACT `DESADV` Pipeline to S/4HANA `DELVRY03` IDoc with Cold-Chain Quarantine & DLQ | Pharma Logistics & EWM |

---

## 🛠️ Core Technical Competencies

- **SAP BTP Integration Suite:** Cloud Integration (CPI), API Management (APIM), Trading Partner Management (TPM), Integration Assessment (ISA-M), SAP Advanced Event Mesh (AEM), Edge Integration Cell (EIC), SAP Graph, Open Connectors.
- **Master Data Governance & Regulatory Domain Models:** SAP MDG / MDG-F / MDG-S / Master Data Integration (MDI), SAP One Domain Model (ODM), S/4HANA 2025 OData V4 (`API_BUSINESS_PARTNER`, `API_PRODUCT_SRV`, `A_GLAccountInChartOfAccounts`, `A_BusinessPartnerTaxNumber`), EU ViDA (Directive 2025/516), SAP Green Ledger (EU CSRD / ESRS E1), EU ESPR Digital Product Passports (W3C JSON-LD VC), EU CSDDD & EUDR WGS84 GeoJSON Traceability, ISO 17442 LEI, GS1 Digital Link & GTIN-14 Mod-10, EU REACH Article 33 SVHC Gating, SHA-256 Golden Record Fingerprinting.
- **Development & Automated QA:** Groovy 3 (`java.io.Reader` Streaming), XSLT 3.0, Apache Camel Expression Language, Spock Framework BDD/TDD (`Message` Interface Mocking), Gradle, SonarQube, GitHub Actions, SAP Project Piper (`cpiArtifactDeploy`).
- **Protocols & Security:** OData V4/V2, GraphQL, REST/OpenAPI 3.1, SOAP XI 3.0/WS-Security, AS2, OASIS AS4 (Peppol), SFTP, AMQP/JMS, Kafka, IDoc/RFC, Cloud Connector Principal Propagation, mTLS X.509, OAuth 2.0 (RFC 8693), OpenPGP, NIST Post-Quantum Cryptography (`ML-KEM-768` / `ML-DSA-65`).
