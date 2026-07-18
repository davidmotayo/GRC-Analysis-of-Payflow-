# END-TO-END SECURITY GOVERNANCE PLAN

## 1. Introduction and Programme Mandate

This Security Governance Plan is the final, consolidating deliverable of PayFlow Fintech Nigeria Ltd.'s eight-week GRC programme. It is the document that a certification body would first request during a Stage 1 documentation audit. It brings together every element of the ISMS programme into a single authoritative reference: governance structure, risk posture, policy framework, audit findings, treatment commitments, and the certification roadmap.

PayFlow is a Lagos-based fintech startup processing thousands of daily financial transactions across card, bank transfer, and mobile wallet channels. At the outset of this programme, the organisation had no formalised security governance, no documented risk management process, no security policies, and no incident response capability. The GRC programme has changed that — establishing the foundation upon which a certified ISMS can be built.

This document is the authoritative ISMS foundation record for PayFlow and should be reviewed by the Board, maintained by the CISO, and updated at minimum annually or upon any significant change to PayFlow's technology infrastructure, regulatory environment, or risk profile.

## 2. ISMS Scope Statement

The following scope statement fulfils ISO/IEC 27001:2022 Clause 4.3 and must be formally approved by the CEO/CTO before any certification audit proceeds.

| Parameter | Definition |
|---|---|
| Organisation | PayFlow Fintech Nigeria Ltd., incorporated and operating in Lagos, Nigeria. |
| ISMS Scope | All information systems, applications, cloud infrastructure, backend APIs, payment processing pipelines, customer PII databases, employee endpoints, and third-party integrations used by PayFlow to deliver its digital payment services to merchants and consumers. |
| Locations | Primary: Lagos, Nigeria (Ikorodu area). Cloud: Amazon Web Services (AWS) / Google Cloud Platform — Nigeria and adjacent regions. Remote working endpoints: Nigeria. |
| Included Assets | Cloud VMs and managed services; backend payment APIs; customer PII (names, phone, email, partial financial data); cloud storage (logs and backups); third-party payment processor integrations; developer credentials and API keys; employee devices and endpoints; source code repositories; administrative accounts; internal communication channels. |
| Exclusions | Physical infrastructure of cloud providers (AWS/GCP) — managed under their ISO 27001 certified environment and addressed through supplier controls A.5.19–A.5.23. Outsourced software development — no current engagements. |
| Applicable Standards | ISO/IEC 27001:2022 (primary); PCI DSS v4.0; Nigeria Data Protection Act 2023; NDPC GAID 2025; CBN Risk-Based Cybersecurity Framework 2024; Nigeria Cybercrimes Act (Amended 2024). |
| ISMS Version | Version 1.0 — Initial ISMS establishment. This is the first formal ISMS for PayFlow. |

## 3. Information Security Policy Statement

The following policy statement must be approved and signed by the CEO before this document becomes effective. It fulfils ISO/IEC 27001:2022 Clause 5.2 and Annex A.5.1.

> **PAYFLOW FINTECH — INFORMATION SECURITY POLICY**
> Version 1.0 | Approved by: CEO / CTO | Classification: Internal
>
> PayFlow Fintech Nigeria Ltd. is committed to protecting the confidentiality, integrity, and availability of all information assets entrusted to us by our customers, partners, employees, and regulators.
>
> We will:
> - Manage information security risk through a systematic, evidence-based ISMS aligned with ISO/IEC 27001:2022.
> - Comply with all applicable Nigerian laws and regulations including the NDPA 2023, CBN Cybersecurity Framework 2024, and the Cybercrimes Act 2024.
> - Grant access to information assets on a least-privilege, need-to-know basis only, as defined in our Access Control Policy (POL-SEC-002).
> - Ensure all staff are trained in their information security responsibilities and understand the consequences of policy violations.
> - Detect, respond to, and learn from security incidents in a timely and structured manner, fulfilling all regulatory notification obligations.
> - Continually improve the ISMS through regular risk assessments, internal audits, and management reviews, pursuant to ISO 27001:2022 Clauses 9 and 10.
> - Protect the personal data of our customers as required by the NDPA 2023 and GAID 2025, treating privacy as a fundamental right and business obligation.
>
> This policy applies to all PayFlow employees, contractors, temporary staff, and third parties with access to PayFlow systems or data. Violations will be subject to disciplinary action as defined in our Security Policies.
>
> CEO Signature: _________________________ CTO Signature: _________________________ Date: _______________

## 4. ISMS Governance Structure

The following governance structure defines accountability for the ISMS across PayFlow's organisation. All role holders must formally acknowledge their responsibilities in writing as part of the ISMS onboarding process.

| ISMS Role | Position | Responsibilities |
|---|---|---|
| ISMS Owner | Chief Executive Officer (CEO) | Ultimate accountability for the ISMS. Signs the Information Security Policy. Chairs quarterly management review. Approves residual risk acceptance for HIGH and CRITICAL risks. Represents PayFlow in regulatory engagement. |
| ISMS Custodian | Chief Information Security Officer (CISO) | Day-to-day management of the ISMS programme. Reviews and updates ISMS documentation. Approves exceptions to policies. Leads internal audit programme. Submits annual cybersecurity report to CBN. Signs Statement of Applicability. |
| GRC Analyst | GRC Analyst | Maintains Risk Register, Risk Matrix, and Compliance Checklist. Coordinates internal audits. Tracks corrective action closure. Prepares management review inputs. Supports regulatory submissions (NDPC, CBN). Updates SoA and RTP. |
| Risk Owners | Department Heads (CTO, Engineering Lead, IT Admin, HR, Legal) | Own identified risks within their domain. Implement assigned corrective actions. Report treatment progress monthly to GRC Analyst. Escalate blockers to CISO within 48 hours. |
| Data Protection Officer (DPO) | DPO (to be appointed) | Oversees NDPA 2023 compliance. Handles NDPC registration and regulatory submissions. Manages data subject rights requests. Conducts DPIAs for new processing activities. Required appointment under NDPA 2023. |
| IT / DevOps Team | IT Administrator / DevOps Lead | Implements technical controls (MFA, RBAC, SIEM, CSPM, MDM, encryption). Maintains access register. Executes access provisioning and deprovisioning per POL-SEC-002. Manages cloud security configuration. |
| All Staff | All Employees & Contractors | Comply with all ISMS policies. Complete mandatory security awareness training. Report suspected security incidents immediately. Protect credentials and physical assets per policy. |

## 5. Risk Management Methodology

PayFlow's risk management process follows a qualitative methodology aligned with ISO/IEC 27001:2022 Clause 6.1.2. The process is continuous — risks are identified, assessed, treated, monitored, and reviewed on a scheduled and event-triggered basis.

| Step | Activity | Frequency / Trigger |
|---|---|---|
| 1 | Asset & Threat Identification — Identify all assets, applicable threats, and inherent risks (RISK-REG-001) | Annually + upon significant infrastructure or business change |
| 2 | Risk Assessment — Score each risk using Likelihood × Impact (1–5 scale) on a 5×5 matrix (RISK-MAT-001) | Annually + after any Major NC is identified |
| 3 | Risk Treatment — Select treatment option (Mitigate / Accept / Transfer / Avoid); implement controls; document in RTP-001 | Following each risk assessment; reviewed every 6 months |
| 4 | Control Implementation — Deploy Annex A controls per the SoA and corrective action plans | Continuous — tracked against target dates in corrective action register |
| 5 | Monitoring & Review — SIEM alerts, access reviews, KPI dashboards, management review (Clause 9.3) | KPIs: monthly. Access reviews: quarterly. Management review: quarterly. |
| 6 | Internal Audit — Formal audit of ISMS conformance and control effectiveness (AUD-RPT-001) | Annually (mandatory per Clause 9.2) + following a Major incident |
| 7 | Continual Improvement — Address nonconformities, update policies, apply lessons learned (Clause 10) | Ongoing; documented in corrective action register |

## 6. Consolidated Risk Register

The table below is the master risk register for PayFlow — consolidating Week 1 (identification), Week 2 (scoring), and Week 6 (treatment) into a single live document. It is the primary operational tool of the ISMS and must be reviewed and updated quarterly by the GRC Analyst.

| ID | Risk Name | L | I | Treatment | Residual | Owner | Target | NC Ref |
|---|---|---|---|---|---|---|---|---|
| R001 | API Key / Credential Exposure | 5 | 5 | MITIGATE | LOW | Eng. Lead | 7 Days | NC-005 |
| R002 | PII & Financial Data Unencrypted | 4 | 5 | MITIGATE | MEDIUM | DevOps | 7 Days | NC-009 |
| R003 | Unrestricted Production Access | 4 | 5 | MITIGATE | MEDIUM | CTO | 30 Days | NC-003 |
| R004 | Inconsistent MFA | 4 | 4 | MITIGATE | LOW | IT Admin | 7 Days | NC-004 |
| R005 | Unsecured Payment APIs | 3 | 5 | MITIGATE | MEDIUM | Eng. Lead | 60 Days | OFI-002 |
| R006 | Third-Party / Supply Chain | 3 | 5 | MITIGATE+TRANSFER | MEDIUM | Legal/CTO | 45 Days | NC-010 |
| R007 | No Incident Response Plan | 3 | 5 | MITIGATE | MEDIUM | CISO | 30 Days | NC-007 |
| R008 | Insider Threat / No Training | 3 | 4 | MITIGATE | MEDIUM | HR | 30 Days | NC-008 |
| R009 | No Formal ISMS / Governance | 5 | 3 | MITIGATE | MEDIUM | CISO | 30 Days | NC-001/002 |
| R010 | Cloud Misconfiguration | 3 | 4 | MITIGATE | LOW | DevOps | 30 Days | NC-006 |
| R011 | Phishing / Social Engineering | 4 | 3 | MITIGATE | MEDIUM | IT Admin | 45 Days | OFI-004 |
| R012 | Reputational / Investor Risk | 4 | 3 | ACCEPT+MITIGATE | MEDIUM | CEO | 60 Days | — |

## 7. Security Policy Suite

The following policies constitute PayFlow's formal security policy framework. Policies marked PUBLISHED are active and enforceable. Policies marked IN DEVELOPMENT are part of the ISMS implementation roadmap and must be completed before Stage 1 certification audit.

| Doc ID | Policy Name | Owner | Status | Scope & Key Provisions |
|---|---|---|---|---|
| POL-SEC-001 | Password Policy | CISO / IT Admin | COMPLETE | Minimum 12-char passwords (16 for admin); complexity requirements; 90-day expiry; 10-password history; MFA mandatory; secrets manager required for API keys; prohibition on shared credentials. Governs all 45 PayFlow accounts. |
| POL-SEC-002 | Access Control Policy | CISO / IT Admin | COMPLETE | Least-privilege and default-deny principles; RBAC matrix (9 roles × 8 systems); 5-step provisioning and deprovisioning processes; 4-hour account disabling SLA on departure; quarterly privileged access reviews; PAM controls; production environment restrictions; anomaly detection requirements. |
| POL-SEC-003 | Acceptable Use Policy | HR / CISO | PLANNED | Permitted use of company systems, devices, and data; prohibited activities; personal device policy; social media and external communications; consequences of violation. Required before Clause 7.3 awareness can be evidenced. |
| POL-SEC-004 | Data Classification Policy | GRC Analyst / DPO | PLANNED | Four-tier classification: Public / Internal / Confidential / Restricted; labelling standards; handling requirements per tier; retention schedules; disposal procedures. Required for NDPA 2023 and A.5.12 compliance. |
| POL-SEC-005 | Cryptographic Standards Policy | CTO / DevOps | PLANNED | Approved algorithms (AES-256 at rest; TLS 1.2+ in transit; RSA-2048 minimum); key management; certificate lifecycle; prohibition of deprecated algorithms (MD5, SHA-1, DES). Required for A.8.24 and PCI DSS Req. 3. |
| POL-SEC-006 | Incident Response Plan (IRP) | CISO | PLANNED | 6-phase IRP: Preparation → Identification → Containment → Eradication → Recovery → Lessons Learned; IR team roles; 72-hour regulatory notification procedure (Cybercrimes Act 2024); NDPC breach notification (NDPA 2023 S.40(2)); evidence collection; tabletop exercise schedule. |
| POL-SEC-007 | Remote Working Policy | CISO / IT Admin | PLANNED | VPN requirements; approved device types; home network security; MFA for all remote sessions; prohibition of public Wi-Fi without VPN; screen lock; data handling restrictions when off-premises. |
| POL-SEC-008 | Vendor & Third-Party Security Policy | GRC Analyst / Legal | PLANNED | Vendor risk assessment framework; security SLA requirements; right-to-audit clause; data breach notification obligations (72-hr); required certifications (SOC 2 Type II or ISO 27001); annual review cadence. |
| POL-SEC-009 | Change Management Policy | CTO / DevOps | PLANNED | Formal change request and approval process; mandatory security review for changes to production systems; rollback procedure; emergency change protocol; prohibition of direct production deployments without review. |
| POL-SEC-010 | Business Continuity Policy | CEO / CTO | PLANNED | RTO and RPO targets for all critical systems; BCP roles and responsibilities; backup schedule and restoration testing (quarterly); failover configuration; crisis communications; alignment with IRP. |

## 8. Corrective Action Tracker

The corrective action tracker below consolidates all 19 findings from the Week 5 internal audit (AUD-RPT-001). This is the live operational document that the GRC Analyst updates weekly and presents to the CISO monthly. Each finding must be closed with documented evidence before it can be marked RESOLVED.

| ID | Domain | Type | Corrective Action Required | Owner | Target Date | Status | Evidence Required |
|---|---|---|---|---|---|---|---|
| NC-001 | ISMS Governance | MAJOR NC | Draft and publish Information Security Policy; define ISMS scope; establish ISMS governance RACI | CEO/CISO | 30 Days | NOT STARTED | Signed policy; scope document; RACI published |
| NC-002 | Risk Management | MAJOR NC | Produce Risk Treatment Plan (RTP-001) and Statement of Applicability (SOA-001) | CISO | 30 Days | COMPLETE | RTP-001 and SOA-001 documents (Week 6) |
| NC-003 | Access Control | MAJOR NC | Revoke developer production access; implement RBAC; deploy environment separation | CTO | 7 Days | NOT STARTED | Access audit log; RBAC config; env. architecture diagram |
| NC-004 | Identity Management | MAJOR NC | Enforce MFA for all 45 accounts via Conditional Access policy | IT Admin | 7 Days | NOT STARTED | Identity provider export showing 100% MFA enrolment |
| NC-005 | Secrets Hygiene | MAJOR NC | Deploy secrets manager; rotate all API keys; implement pre-commit scanning | Eng. Lead | Immediate | NOT STARTED | Secrets manager deployment record; key rotation log; CI/CD scan config |
| NC-006 | Monitoring | MAJOR NC | Enable CloudTrail; deploy SIEM; configure alerting rules; enforce log retention | DevOps | 30 Days | NOT STARTED | SIEM deployment evidence; CloudTrail enabled; alert rule documentation |
| NC-007 | Incident Response | MAJOR NC | Develop, publish, and test Incident Response Plan (POL-SEC-006) | CISO | 30 Days | NOT STARTED | Published IRP; tabletop exercise record; IR team role confirmations |
| NC-008 | People Security | MAJOR NC | Launch security awareness training for all 45 staff; integrate into onboarding | HR | 30 Days | NOT STARTED | Training completion records for all 45 staff; LMS records |
| NC-009 | Data Protection | MAJOR NC | Enable AES-256 encryption on all cloud buckets and databases; conduct DPIA; register with NDPC | DevOps | 7 Days | NOT STARTED | Encryption audit; DPIA document; NDPC registration confirmation |
| NC-010 | Vendor Risk | MAJOR NC | Establish vendor risk register; update contracts with security SLAs and NDPA clauses | Legal | 45 Days | NOT STARTED | Vendor risk register; updated contract excerpts |
| NC-011 | Performance | MINOR NC | Define security KPI framework; configure cloud capacity alerting | CISO | 60 Days | NOT STARTED | KPI dashboard; alerting configuration |
| NC-012 | Physical Security | MINOR NC | Publish Clear Desk Policy; enforce 5-min screen lock via MDM | IT Admin | 45 Days | NOT STARTED | Published policy; MDM configuration screenshot |
| NC-013 | Asset Management | MINOR NC | Create and maintain formal asset register for all hardware, software, and cloud assets | IT Admin | 45 Days | NOT STARTED | Asset register; quarterly review confirmation |
| NC-014 | Business Continuity | MINOR NC | Conduct and document full backup restoration test; schedule quarterly | IT Admin | 30 Days | NOT STARTED | Restoration test report with timestamp and results |
| NC-015 | Compliance | MINOR NC | Compile regulatory contact register: NDPC, CBN, NCAC, law enforcement | Legal | 45 Days | NOT STARTED | Published contact register integrated into IRP |

## 9. Nigerian Regulatory Compliance Obligations

PayFlow operates at the intersection of four major Nigerian and international regulatory frameworks. The following section documents each obligation, PayFlow's current compliance posture, and the specific actions required to achieve and maintain compliance.

### 9.1 Nigeria Data Protection Act (NDPA) 2023 & GAID 2025

The NDPA 2023 is Nigeria's primary data protection legislation, administered by the National Data Protection Commission (NDPC). PayFlow qualifies as both a Data Controller and Data Processor under the Act, and based on transaction volumes, likely meets the threshold for registration as a Data Controller and Processor of Major Importance (DCPMI).

| Obligation | PayFlow Position & Required Action |
|---|---|
| DCPMI Registration | PayFlow likely meets the DCPMI threshold. Registration with NDPC is mandatory. A late registration fee applies (deadline was October 2024). Action: Submit registration within 7 days. |
| Data Protection Officer (DPO) | A DPO must be appointed and registered with the NDPC. The DPO must be accessible to data subjects and the NDPC. Action: Appoint DPO within 30 days; register with NDPC. |
| Data Protection Impact Assessment (DPIA) | A DPIA is required before processing activities that present high risk to data subjects — PayFlow's payment processing qualifies. Action: Conduct DPIA within 30 days. Document and maintain on file. |
| Lawful Basis for Processing | PayFlow must document the lawful basis for every category of personal data processed. GAID 2025 specifies documentation standards. Action: Compile data processing records (Record of Processing Activities — ROPA) aligned with GAID 2025 requirements. |
| Data Subject Rights | PayFlow must be able to respond to access, correction, deletion, and portability requests within 72 hours. Action: Implement a data subject rights request procedure and designate the DPO as the point of contact. |
| Breach Notification | Personal data breaches must be reported to the NDPC within 72 hours of discovery. Action: Incorporate NDPC notification procedure into the Incident Response Plan (POL-SEC-006). |
| Cross-Border Data Transfers | Personal data transferred outside Nigeria requires NDPC approval or adequate safeguards. GAID 2025 specifies the documentation required. Action: Audit all data flows involving cloud providers and payment processors for cross-border transfers. |
| Technical & Organisational Measures | The NDPA requires measures proportionate to data sensitivity — encryption is explicitly required. Action: AES-256 encryption on all PII (NC-009 corrective action). Cryptographic Standards Policy required. |

### 9.2 CBN Risk-Based Cybersecurity Framework 2024

The CBN's cybersecurity framework applies to all payment service entities operating in Nigeria. PayFlow's payment processing activities bring it within scope. Key obligations include:

- **Annual CISO Cybersecurity Report:** Due 31 March each year. PayFlow must submit a formal cybersecurity posture report signed by the CISO to the CBN. This is the first year of this obligation for PayFlow.
- **Third-Party Risk Management:** CBN explicitly requires assessment and management of cybersecurity risks in the payment supply chain. Directly maps to R-006 and NC-010 in the PayFlow corrective action register.
- **Access Control and Identity Management:** The framework mandates multi-factor authentication and least-privilege access for all payment system users. Directly maps to R-003 and R-004.
- **Logging and Monitoring:** Real-time monitoring of payment systems is required. A SIEM or equivalent monitoring capability must be deployed. Directly maps to R-010 and NC-006.
- **Incident Reporting:** Payment-related cybersecurity incidents must be reported to the CBN within timelines defined in the framework. This must be incorporated into the IRP.

### 9.3 Nigeria Cybercrimes Act (Amended 2024)

The 2024 amendment to the Cybercrimes Act introduces a mandatory 72-hour incident reporting obligation for organisations experiencing a cybersecurity incident. PayFlow's confirmed API key exposure (Risk R-001) should have triggered this obligation but was not reported due to the absence of an IRP.

- **72-Hour Reporting:** All cybersecurity incidents must be reported to the relevant authority (Nigerian Cybercrime Advisory Council / relevant agency) within 72 hours of discovery. Action: Incorporate this procedure into the IRP.
- **Incident Classification:** The Act defines categories of cybercrime — PayFlow must understand which categories apply to its environment and ensure appropriate internal classification procedures.
- **Evidence Preservation:** Digital evidence must be preserved in a forensically sound manner for potential legal proceedings. Action: Implement evidence collection procedures (A.5.28) in the IRP.

### 9.4 PCI DSS v4.0

PayFlow processes cardholder data through payment APIs and must comply with PCI DSS. The ISO 27001 controls programme significantly supports PCI DSS compliance but does not replace it. A dedicated QSA-led gap assessment is required.

| Req. | PCI DSS Requirement | PayFlow Gap & Mapping to ISMS Controls |
|---|---|---|
| Req. 1 | Install and maintain network security controls | No network segmentation (NC-003). Maps to A.8.20, A.8.22 — environment separation and network security controls. |
| Req. 2 | Apply secure configurations to all system components | No configuration baselines (NC-006 / R-010). Maps to A.8.9 — CIS Benchmark deployment required. |
| Req. 3 | Protect stored account data | PII and financial data unencrypted (NC-009 / R-002). Maps to A.8.24, A.5.34 — AES-256 encryption mandatory. |
| Req. 6 | Develop and maintain secure systems and software | No Secure SDLC; no SAST/DAST in CI/CD (R-005). Maps to A.8.25–A.8.29 — Secure SDLC implementation required. |
| Req. 7 | Restrict access to system components | Unrestricted developer production access (NC-003 / R-003). Maps to A.5.15, A.8.3 — RBAC mandatory. |
| Req. 8 | Identify users and authenticate access | 28 of 45 accounts lack MFA (NC-004 / R-004). Maps to A.8.5, A.5.17 — MFA enforcement mandatory. |
| Req. 10 | Log and monitor all access to system components | No SIEM; incomplete logging (NC-006 / R-010). Maps to A.8.15, A.8.16 — centralised logging mandatory. |
| Req. 12 | Support information security with organisational policies | No ISMS policy suite (NC-001 / R-009). Maps to A.5.1, A.5.37 — policy suite required for certification. |

## 10. ISMS Operational Calendar

The following calendar defines all recurring ISMS activities, their frequency, owner, and the ISO 27001 clause or control they fulfil. This calendar must be embedded in PayFlow's operational rhythm from Month 1 of implementation.

| Frequency | Activity | Owner | ISO 27001 Ref | Output / Evidence |
|---|---|---|---|---|
| Daily | Review SIEM alerts and security monitoring dashboard | IT Admin / DevOps | A.8.16 | Alert review log; escalation record for any incidents triggered |
| Weekly | Review MFA adoption rate and access provisioning queue | IT Admin | A.8.5 / A.5.16 | Weekly metrics report to CISO; escalation of any non-enrolments |
| Weekly | GRC Analyst NC corrective action status update | GRC Analyst | Cl. 10.2 | Updated corrective action tracker; status reported to CISO |
| Monthly | Security KPI dashboard review and management briefing | CISO | Cl. 9.1 | KPI report; management briefing record; any exceptions documented |
| Monthly | Phishing simulation run and results analysis | GRC Analyst / HR | A.6.3 | Simulation report; click rate; follow-up training triggered for failures |
| Quarterly | Privileged access review (all admin and cloud accounts) | IT Admin / CISO | A.5.18 | Access review sign-off sheet; revocations logged in access register |
| Quarterly | Standard user access review (all non-privileged accounts) | IT Admin / Managers | A.5.18 / POL-SEC-002 | Access review sign-off; any anomalies investigated and documented |
| Quarterly | Vendor / third-party security review (Tier-1 vendors) | GRC Analyst / Legal | A.5.22 | Vendor review report; contract update log; risk register updated |
| Quarterly | ISMS Management Review meeting (Clause 9.3) | CEO / CISO | Cl. 9.3 | Board-level meeting minutes; decisions on ISMS objectives and resources |
| Quarterly | Backup restoration test and documentation | IT Admin | A.8.13 | Restoration test report with RTO measurement; archived for audit |
| Semi-Annually | Risk register and risk matrix review | GRC Analyst / CISO | Cl. 6.1.2 | Updated risk register; new or changed risks assessed; RTP updated |
| Semi-Annually | SoA and RTP review | CISO / GRC Analyst | Cl. 6.1.3 | Updated SOA-001 and RTP-001; version-controlled and signed off |
| Annually | Full internal ISMS audit (all clauses and Annex A controls) | GRC Analyst / External Auditor | Cl. 9.2 | Audit findings report; corrective action register updated |
| Annually | Security awareness training refresh for all staff | HR / GRC Analyst | A.6.3 | Training completion records; annual attestation signed by all staff |
| Annually | Full cloud configuration and security posture audit | DevOps / External Assessor | A.5.23 / A.8.9 | Cloud audit report; CIS benchmark compliance score; remediation plan |
| Annually | CBN Annual Cybersecurity Report submission | CISO | CBN Framework 2024 | Submitted report; CBN acknowledgement; copy retained for ISMS evidence |
| Annually | NDPC DCPMI status review and re-registration if required | DPO / Legal | NDPA 2023 | NDPC registration confirmation; DPO registration renewal |
| As triggered | Incident response activation and post-incident review | CISO / IR Team | A.5.24–A.5.27 | Incident log; PIR report; lessons learned; regulatory notifications filed |
| As triggered | Emergency change management process | CTO / CISO | A.8.32 | Emergency change record; post-change security review; rollback test |

## 11. Security Objectives and KPIs

The following measurable security objectives fulfil ISO/IEC 27001:2022 Clause 6.2. They must be tracked monthly and reported to the board quarterly. Baseline is set at programme completion (current state). Targets are for Month 3, Month 6, and Month 9.

| Security Objective / KPI | Baseline | Month 3 | Month 6 | Month 9 | Measurement Method |
|---|---|---|---|---|---|
| MFA adoption rate (all accounts) | 62% | 100% | 100% | 100% | Identity provider monthly report |
| Open CRITICAL risks (score ≥ 20) | 3 | 0 | 0 | 0 | Risk register quarterly review |
| Open HIGH risks (score 12–19) | 9 | 5 | 1 | 0 | Risk register quarterly review |
| Staff security training completion | 0% | 100% | 100% | 100% | LMS training records |
| Phishing simulation click rate | Baseline TBD | < 15% | < 10% | < 5% | Quarterly phishing simulation report |
| Cloud storage encryption coverage | 62.5% | 100% | 100% | 100% | Monthly cloud configuration audit |
| Major NC corrective actions closed | 0 of 10 | 8 of 10 | 10 of 10 | 10 of 10 | Corrective action tracker (weekly) |
| Security policies published | 2 of 10 | 6 of 10 | 9 of 10 | 10 of 10 | Policy register |
| Vendor security assessments complete | 0 of 3 | 2 of 3 | 3 of 3 | 3 of 3 | Vendor risk register |
| Mean Time to Detect (MTTD) — incidents | Not measurable | < 24 hrs | < 4 hrs | < 1 hr | SIEM alerting metrics |
| Mean Time to Respond (MTTR) — incidents | Not measurable | < 72 hrs | < 24 hrs | < 4 hrs | Incident log and IRP timer records |
| ISMS documentation completeness | 25% | 60% | 85% | 100% | GRC Analyst quarterly audit |
| ISO 27001 control implementation | 9% | 40% | 75% | 95% | SoA implementation status update |

## 12. ISO/IEC 27001:2022 Certification Roadmap

The following roadmap defines the structured path from PayFlow's current state — Level 1 ISMS maturity with 10 Major Nonconformities — to ISO/IEC 27001:2022 certification. It is the operational implementation guide for the entire ISMS programme and should be reviewed monthly by the CISO and quarterly by the board.

### Phase 1: Foundation (Months 1–2)

**Deliverables & Milestones:**
- Information Security Policy signed and published
- ISMS scope document approved
- ISMS governance structure (RACI) published
- All 10 Major NC corrective actions initiated
- MFA enforced: 100% of all accounts
- Developer production access revoked; RBAC implemented
- AES-256 encryption enforced on all cloud buckets and databases
- Secrets manager deployed; all API keys rotated
- NDPC DCPMI registration submitted
- DPO appointed and registered with NDPC

**Success Criteria:** 0 CRITICAL risks without active corrective action. MFA: 100% adoption. All PII encrypted. NDPC registration confirmed. DPO registered.

### Phase 2: Core Controls (Months 2–4)

**Deliverables & Milestones:**
- SIEM deployed with live alerting rules
- IRP published, IR team assigned, tabletop exercise completed
- Security awareness training: all 45 staff completed (LMS records)
- DPIA completed and filed
- Network segmentation implemented (dev/staging/prod separated)
- SAST and DAST integrated into CI/CD pipeline
- Vendor risk register established; Tier-1 contracts updated with security SLAs
- DNS-based web filtering and EDR deployed on all endpoints
- Backup restoration test conducted and documented

**Success Criteria:** SIEM operational. Training completion 100%. IRP tested via tabletop. Network segmentation confirmed. PCI DSS Req. 7 & 8 partially met.

### Phase 3: Governance (Months 4–6)

**Deliverables & Milestones:**
- Full 10-policy suite published (POL-SEC-001 to POL-SEC-010)
- First quarterly access review completed and signed off
- First quarterly management review meeting minuted
- Asset register complete and current
- Cryptographic Standards Policy in effect
- PCI DSS gap assessment completed (external QSA)
- CBN Annual Cybersecurity Report drafted (if Q1 deadline applicable)
- All 10 Major NCs: closed with documented evidence
- All 5 Minor NCs: resolved or formally accepted
- KPI dashboard operational

**Success Criteria:** All Major NCs closed. All policies published. Management reviews active. PCI DSS gap report available. Full SoA in IN PROGRESS or COMPLETE.

### Phase 4: Certification (Months 7–9)

**Deliverables & Milestones:**
- Pre-audit readiness review (internal gap check against full ISO 27001 checklist)
- Stage 1 Documentation Audit — external certification body reviews all ISMS documents
- Stage 1 findings addressed and evidenced
- Stage 2 Certification Audit — on-site assessment of control implementation
- Any Minor NCs from Stage 2 closed within agreed timeframe
- ISO/IEC 27001:2022 Certificate issued
- Surveillance audit programme established (annual, 3-year cycle)

**Success Criteria:** Certificate issued. Zero open Major NCs. 95%+ SoA controls implemented. Surveillance audit scheduled. CBN and NDPC notified of certification.

## 13. Continual Improvement Framework

ISO/IEC 27001:2022 Clause 10 requires that PayFlow continually improves the suitability, adequacy, and effectiveness of the ISMS. The Plan-Do-Check-Act (PDCA) cycle is the operational model for this improvement process.

| PDCA Phase | ISMS Activity | PayFlow Implementation |
|---|---|---|
| PLAN | Risk assessment, objective setting, treatment planning | Annual risk assessment; security objectives (Section 11); Risk Treatment Plan (RTP-001); SoA (SOA-001); ISMS scope review |
| DO | Implement controls, train staff, deploy tooling | Corrective action execution per tracker (Section 8); security awareness training; technical control deployment per RTP-001 |
| CHECK | Internal audit, management review, KPI monitoring | Annual internal audit (Clause 9.2); quarterly management review (Clause 9.3); monthly KPI dashboard; SIEM monitoring |
| ACT | Address nonconformities, apply lessons learned, update ISMS | Corrective action closure; post-incident reviews; policy updates; risk register refresh; SoA updates; board reporting |

## 14. Document Control and Version Management

All ISMS documents must be version-controlled, reviewed on schedule, and maintained in a central ISMS document register. The following master document register covers all GRC programme deliverables.

| Doc ID | Document Name | Version | Owner | Review Cycle | Last Reviewed / Status |
|---|---|---|---|---|---|
| GRC-FINAL-001 | Security Governance Plan (this document) | 1.0 | CISO | Annual | Current — pending board approval |
| RISK-REG-001 | Risk Register | 1.0 | GRC Analyst | Quarterly | Week 1 — due for first quarterly update Month 3 |
| RISK-MAT-001 | Risk Assessment & Matrix | 1.0 | GRC Analyst | Semi-Annual | Week 2 — due for update Month 6 |
| POL-SEC-001 | Password Policy | 1.0 | CISO / IT Admin | Annual | Week 3 — published, enforced pending MFA rollout |
| POL-SEC-002 | Access Control Policy | 1.0 | CISO / IT Admin | Annual | Week 3 — published, RBAC enforcement in progress |
| POL-SEC-003 to 010 | Pending Policy Suite (8 policies) | Draft | Various | Annual | IN DEVELOPMENT — target completion Month 3 |
| GRC-CHK-001 | ISO 27001 Compliance Checklist | 1.0 | GRC Analyst | Annual (with each audit) | Week 4 — to be updated after Month 3 control implementation |
| AUD-RPT-001 | Internal Audit Findings Report | 1.0 | GRC Analyst | Annual | Week 5 — all corrective actions in progress |
| RTP-001 | Risk Treatment Plan | 1.0 | CISO | Semi-Annual | Week 6 — implementation not yet started for most risks |
| SOA-001 | Statement of Applicability | 1.0 | CISO | Semi-Annual | Week 6 — 90 controls included, 3 excluded; implementation 9% |
| EXEC-RPT-001 | Executive Compliance Report | 1.0 | GRC Analyst | Quarterly | Week 7 — for board review |

## 15. Programme Completion Statement

This Security Governance Plan marks the completion of PayFlow Fintech Nigeria Ltd.'s eight-week GRC programme. The programme was designed to take a fintech startup with no formal security governance and establish a documented, auditable, and actionable ISMS foundation in eight structured weeks.

**WHAT THIS PROGRAMME HAS DELIVERED**

- A comprehensive risk picture — 12 risks scored, prioritised, and owned across 4 categories
- The first two formal security policies in PayFlow's history — Password and Access Control
- A complete ISO/IEC 27001:2022 compliance map across all 93 Annex A controls
- The first internal audit ever conducted at PayFlow — 19 findings, all documented with evidence
- A formal Risk Treatment Plan and Statement of Applicability — the twin pillars of ISO 27001 Clause 6.1.3
- A board-ready compliance report synthesising all programme findings for executive decision-making
- This document — a complete, certification-ready ISMS foundation that a Stage 1 auditor can review

PayFlow began this programme with no security policies, no risk assessments, no audit history, and no regulatory compliance framework. It now has a documented ISMS foundation, a clear certification roadmap, named risk owners, a corrective action tracker, and a governance structure that the board can hold itself accountable to. The next step is execution.

## 16. Final Programme Sign-Off

By signing below, the parties confirm that the PayFlow GRC Programme has been completed, all eight deliverables have been produced and reviewed, and the organisation commits to executing the ISMS implementation roadmap defined in this Security Governance Plan.

| Role | Name | Signature / Date |
|---|---|---|
| GRC Analyst (Programme Author) | | |
| Chief Information Security Officer (CISO) | | |
| Chief Technology Officer (CTO) | | |
| Chief Executive Officer (CEO) | | |
| Board Representative / Non-Executive Director | | |
