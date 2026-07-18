# INTERNAL AUDIT FINDINGS REPORT
**PayFlow Fintech Nigeria Ltd. — ISO/IEC 27001:2022 Audit Simulation | GRC Week 5**

## 1. Document Control

| Document Title | Report ID | Version | Classification |
|---|---|---|---|
| Internal Audit Findings Report | AUD-RPT-001 | 1.0 | CONFIDENTIAL |

| Audit Period | Lead Auditor | Audit Standard | Report Date |
|---|---|---|---|
| 26 May 2026 | GRC Analyst (Internal) | ISO/IEC 27001:2022 | 26 May 2026 |

## 2. Audit Scope and Objectives

| Audit Parameter | Detail |
|---|---|
| ISMS Scope | All cloud-hosted information systems, backend APIs, payment processing infrastructure, customer PII databases, cloud storage, and internal tools operated by PayFlow Fintech Nigeria Ltd., Lagos. |
| Domains Audited | ISO/IEC 27001:2022 Clauses 4–10 (ISMS Core Requirements) and all applicable Annex A controls (A.5–A.8) |
| Audit Objectives | (1) Assess conformance with ISO/IEC 27001:2022 requirements; (2) Evaluate effectiveness of controls documented in Weeks 1–4; (3) Identify and classify nonconformities; (4) Issue corrective action recommendations; (5) Assess alignment with NDPA 2023, GAID 2025, and CBN Risk-Based Cybersecurity Framework 2024. |
| Audit Methodology | Document review, evidence collection, system observation, staff interviews, technical spot-checks, and risk register cross-referencing. |
| Audit Criteria | ISO/IEC 27001:2022 standard; PayFlow Risk Register (Wk 1); Risk Assessment (Wk 2); Password Policy POL-SEC-001 (Wk 3); Access Control Policy POL-SEC-002 (Wk 3); ISO 27001 Compliance Checklist GRC-CHK-001 (Wk 4). |
| Regulatory Context | Nigeria Data Protection Act (NDPA) 2023; NDPC General Application and Implementation Directive (GAID) 2025; CBN Risk-Based Cybersecurity Framework for Payment Service Banks 2024; Nigeria Cybercrimes Act (Amended 2024) — 72-hour incident reporting requirement. |
| Auditor Independence | This is a simulated internal audit conducted by the GRC Analyst. The analyst has had no direct operational involvement in the systems under review. |
| Limitations | As a first-cycle audit with no previous ISMS in place, this report documents baseline nonconformities against the standard. No prior audit results were available for comparison. Evidence is assessed from documentation review and technical observation only. |

## 3. Nonconformity Classification System

All audit findings are classified using the standard ISO 27001 internal audit taxonomy below. Classification determines the urgency of the corrective action required and the impact on certification eligibility.

| Type | Classification | Definition |
|---|---|---|
| MAJOR NC | Mandatory — Blocks Certification | A direct failure to meet a mandatory requirement of ISO/IEC 27001:2022. A Major NC must be resolved before certification can be granted. Failure to resolve will result in a failed audit. |
| MINOR NC | Must Resolve — Time-Limited | A partial or isolated failure to meet a requirement. The overall control objective is met, but documentation, evidence, or consistency is lacking. Must be resolved within an agreed timeframe. |
| OFI | Recommended Enhancement | Opportunity for Improvement. No nonconformity exists, but the auditor identifies an enhancement that would improve ISMS effectiveness or reduce risk. |
| COMPLIANT | Satisfactory | The control or requirement is fully implemented, documented, and evidenced to the auditor's satisfaction. |

## 4. Executive Summary

This internal audit of PayFlow Fintech Nigeria Ltd. was conducted against ISO/IEC 27001:2022 — the current version of the standard, to which all organisations must now be certified following the expiry of all 2013 certificates on October 31 2025. The audit identified 19 findings in total, comprising 10 Major Nonconformities, 5 Minor Nonconformities, and 4 Opportunities for Improvement.

The findings confirm that PayFlow is at an early but intentional stage of ISMS implementation. The GRC programme initiated in Week 1 represents the organisation's first structured approach to information security governance. However, the volume and severity of Major Nonconformities — particularly the absence of a formal ISMS, missing incident response capability, inconsistent access controls, and gaps in PII encryption — indicate that significant remediation is required before ISO 27001 certification is achievable.

Critically, several findings also constitute non-compliance with Nigerian regulatory obligations including the NDPA 2023, the GAID 2025, and the CBN Risk-Based Cybersecurity Framework 2024, creating regulatory risk beyond the ISO certification scope.

| Finding Type | Count | % of Total | Implication |
|---|---|---|---|
| MAJOR NC — Blocks Certification | 10 | 53% | All Major NCs must be resolved before ISO 27001 certification can be granted. Immediate remediation required. |
| MINOR NC — Time-Limited Resolution | 5 | 26% | Must be resolved within agreed timeframes and evidenced before or during Stage 2 certification audit. |
| OFI — Opportunity for Improvement | 4 | 21% | No nonconformity — recommended enhancements to improve security posture and ISMS maturity. |
| **TOTAL FINDINGS** | **19** | **100%** | Certification readiness: NOT READY. All Major NCs must be resolved prior to Stage 1 documentation audit. |

**Certification Status:** PayFlow is NOT READY for ISO/IEC 27001:2022 certification at this time. All 10 Major Nonconformities must be fully resolved and supported by documented evidence before a Stage 1 documentation audit can proceed. Estimated readiness: 6–9 months with executive commitment and adequate resource allocation.

## 5. Detailed Audit Findings

The following findings are presented in order of severity — Major Nonconformities first, followed by Minor Nonconformities, and then Opportunities for Improvement.

### 5.1 Major Nonconformities (NC) — Certification Blocking

#### NC-001 | ISMS Scope & Establishment | MAJOR NC

| ISO Clause | Domain | Risk Reference | Owner / Target Date |
|---|---|---|---|
| Cl. 4.3 / 4.4 | ISMS Governance | R-009 | CEO / CISO | < 30 Days |

**Audit Finding:** No Information Security Management System (ISMS) has been established, implemented, or documented. The organisation has no defined ISMS scope statement, no Information Security Policy approved by top management, and no ISMS governance structure. This represents a fundamental non-conformity against the core requirements of the standard.

**Evidence:** No ISMS scope document found. No top-management-approved Information Security Policy in existence. GRC analyst's engagement in this programme represents the first structured security activity. Confirmed by document review and management interviews.

**Corrective Action:** 1. Draft and obtain CEO/CTO sign-off on a formal Information Security Policy. 2. Define and document the ISMS scope covering all cloud systems, APIs, PII, and financial data. 3. Establish an ISMS governance structure with named roles (CISO, GRC Analyst, Risk Owner). 4. Document evidence of management commitment (meeting minutes, signed policy).

#### NC-002 | Risk Treatment Plan | MAJOR NC

| ISO Clause | Domain | Risk Reference | Owner / Target Date |
|---|---|---|---|
| Cl. 6.1.3 / A.5.1 | Risk Management | R-009 | GRC Analyst / CISO | < 30 Days |

**Audit Finding:** No risk treatment plan exists. While a risk register (Wk 1) and risk assessment (Wk 2) have been produced, no formal selection of risk treatment options (mitigate/accept/transfer/avoid) has been documented, and no Statement of Applicability (SoA) exists. ISO 27001 Clause 6.1.3 and certification requirements mandate both.

**Evidence:** Risk Register and Risk Assessment documents reviewed and confirmed as complete. No risk treatment plan document found. No SoA document found. All 12 identified risks remain without formally documented treatment decisions and control mappings.

**Corrective Action:** 1. Produce a formal Risk Treatment Plan mapping each risk to a treatment option and selected controls. 2. Develop a Statement of Applicability (SoA) listing all Annex A controls with applicability justifications. 3. Obtain management sign-off on both documents. 4. Begin implementing treatment actions per the priority action plan.

#### NC-003 | Environment Separation | MAJOR NC

| ISO Clause | Domain | Risk Reference | Owner / Target Date |
|---|---|---|---|
| A.8.31 / A.5.3 | Access & Infrastructure | R-003 | CTO / DevOps Lead | < 1 Week |

**Audit Finding:** No separation exists between development, staging, and production environments. Developers have unrestricted, persistent access to the production environment, including live payment processing systems and customer PII. This is a CRITICAL-priority finding from the risk register (R-003) and a direct violation of A.8.31 and the principle of least privilege.

**Evidence:** System access review confirmed that 11 of 12 developer accounts have read/write access to production cloud infrastructure. No separate production AWS/GCP accounts or VPCs in use. One developer confirmed they had deployed directly to production on three occasions in the past month without any review process. SSH keys for production servers distributed to entire engineering team.

**Corrective Action:** 1. Create separate cloud accounts/projects for dev, staging, and production immediately. 2. Revoke all developer access to production environment pending RBAC implementation. 3. Implement a formal change management and deployment process requiring approvals. 4. Configure production access as time-limited and just-in-time only, logged centrally.

#### NC-004 | Multi-Factor Authentication | MAJOR NC

| ISO Clause | Domain | Risk Reference | Owner / Target Date |
|---|---|---|---|
| A.8.5 / A.5.17 | Identity & Access | R-004 | IT Admin / CISO | < 7 Days |

**Audit Finding:** Multi-Factor Authentication (MFA) is not uniformly enforced across all user accounts. Audit confirmed 28 of 45 staff accounts (62%) do not have MFA enabled. Of the 12 administrative accounts identified, 4 (33%) lack MFA. This directly contravenes the Password Policy (POL-SEC-001) published in Week 3 and violates A.8.5 of ISO 27001:2022.

**Evidence:** Identity provider audit export reviewed. 17 accounts have MFA active; 28 accounts have no MFA configured. Admin account list cross-referenced: 4 admin accounts confirmed without MFA. IT administrator confirmed MFA has not been mandated system-wide and no enforcement campaign has been run since policy publication.

**Corrective Action:** 1. Immediately mandate MFA enforcement through the identity provider (block login without MFA). 2. Enrol all 45 staff within 7 days — prioritise admin accounts first. 3. Configure Conditional Access policies to reject authentication without MFA. 4. Document MFA enrolment status monthly and report to CISO.

#### NC-005 | Secrets & Credential Management | MAJOR NC

| ISO Clause | Domain | Risk Reference | Owner / Target Date |
|---|---|---|---|
| A.8.12 / A.5.17 | Secrets Hygiene | R-001 | Engineering Lead / DevOps | Immediate |

**Audit Finding:** API keys and credentials are not managed through an approved secrets management system. The confirmed incident of an API key exposed on a public GitHub repository (Risk R-001) has not been followed by any formalised corrective action, secrets rotation programme, or pre-commit scanning implementation. Hardcoded credentials found in two active repositories during code review.

**Evidence:** GitHub repository scan conducted during audit: two repositories contain hardcoded AWS access key references in code comments. Secrets Manager tool (AWS Secrets Manager or equivalent) not configured. No pre-commit hooks active on any repository to block secret commits. Incident report for the original API key exposure not found — no documented corrective action.

**Corrective Action:** 1. Immediately rotate all potentially exposed API keys and secrets. 2. Deploy AWS Secrets Manager (or HashiCorp Vault) and migrate all credentials. 3. Configure git-secrets or trufflehog pre-commit hooks on all repositories. 4. Produce a post-incident review for the original exposure event. 5. Add secrets scanning to CI/CD pipeline.

#### NC-006 | Logging & Security Monitoring | MAJOR NC

| ISO Clause | Domain | Risk Reference | Owner / Target Date |
|---|---|---|---|
| A.8.15 / A.8.16 | Security Monitoring | R-010 | DevOps / IT Admin | < 30 Days |

**Audit Finding:** No centralised logging or security monitoring system is in place. Cloud activity logs exist in individual service logs but are not aggregated, monitored, or alerted upon. There is no SIEM, no IDS/IPS, and no defined process for detecting or responding to security events. This leaves PayFlow completely blind to active threats.

**Evidence:** AWS CloudTrail logs exist but are not forwarded to any SIEM. No security alerting rules configured. Cloud storage access logs enabled on only 2 of 8 storage buckets reviewed. No evidence of any security event being detected through internal monitoring in the organisation's history. IT team confirmed no active monitoring dashboard exists.

**Corrective Action:** 1. Enable CloudTrail and VPC Flow Logs across all cloud accounts immediately. 2. Deploy a SIEM solution (AWS Security Hub + CloudWatch, or open-source ELK/Wazuh). 3. Define and configure alerting rules aligned with POL-SEC-002 anomaly detection requirements. 4. Assign a staff member responsible for daily log review. 5. Define log retention at minimum 12 months.

#### NC-007 | Incident Response Plan | MAJOR NC

| ISO Clause | Domain | Risk Reference | Owner / Target Date |
|---|---|---|---|
| A.5.24 / A.5.26 | Incident Management | R-007 | CISO / GRC Analyst | < 30 Days |

**Audit Finding:** No documented Incident Response Plan (IRP) exists. The organisation experienced a real security incident (exposed API key on GitHub) with no formal response, escalation, containment, or post-incident review. This demonstrates both a documentation gap and an operational gap — the control does not exist in either form.

**Evidence:** No IRP document found. Interview with CTO confirmed the API key incident was handled informally via a Slack message. No incident log maintained. No assigned incident response team or roles. No communication protocol or regulatory notification procedure exists, including the 72-hour reporting obligation under the Nigeria Cybercrimes Act (Amended 2024) to relevant authorities.

**Corrective Action:** 1. Develop and publish a formal Incident Response Plan covering: preparation, detection, containment, eradication, recovery, and lessons learned phases. 2. Assign an IR team with named roles (Incident Manager, Technical Lead, Communications Lead). 3. Establish an incident log. 4. Conduct a tabletop exercise within 30 days of IRP publication. 5. Ensure the 72-hour incident notification procedure for Nigerian authorities is documented.

#### NC-008 | Security Awareness Training | MAJOR NC

| ISO Clause | Domain | Risk Reference | Owner / Target Date |
|---|---|---|---|
| A.6.3 / Cl. 7.3 | People & Culture | R-008 | HR / GRC Analyst | < 30 Days |

**Audit Finding:** No security awareness training programme exists. The organisation has grown from 8 to 45 employees with no formal security briefings at onboarding. Staff have not received training on phishing recognition, password hygiene, data handling, or incident reporting. This creates systemic human-factor risk across the entire organisation.

**Evidence:** HR records reviewed: no security training records found for any of the 45 employees. Three staff members interviewed confirmed they had not received any security training since joining. No learning management system (LMS) or training platform in use for security content. Onboarding checklist does not reference security briefing.

**Corrective Action:** 1. Develop a security awareness training programme covering phishing, social engineering, password policy, data classification, and incident reporting. 2. Mandatory completion within 30 days for all 45 existing staff. 3. Integrate into onboarding for all new hires. 4. Run annual refresher training and quarterly phishing simulations. 5. Maintain training completion records for audit evidence.

#### NC-009 | PII Encryption & Data Protection | MAJOR NC

| ISO Clause | Domain | Risk Reference | Owner / Target Date |
|---|---|---|---|
| A.5.34 / A.8.24 | Data Protection | R-002 | DevOps / GRC Analyst / Legal | < 7 Days |

**Audit Finding:** Customer PII and partial financial data are not consistently encrypted at rest. Three of eight cloud storage buckets reviewed contain unencrypted customer data. No formal cryptographic standards policy exists. This violates A.8.24 of ISO 27001:2022 and also constitutes a non-compliance with the Nigeria Data Protection Act (NDPA) 2023, which mandates technical measures including encryption proportionate to data sensitivity.

**Evidence:** Cloud storage bucket audit: 3 buckets with PII content found without server-side encryption enabled. Database review: primary customer database has encryption at rest enabled; two analytical read-replicas do not. No data classification policy to guide encryption decisions. NDPA 2023 registration status with NDPC unconfirmed — PayFlow likely qualifies as a Data Controller and Processor of Major Importance (DCPMI) given volume of financial PII processed.

**Corrective Action:** 1. Enable AES-256 server-side encryption on all cloud storage buckets immediately. 2. Enable encryption on all database replicas within 7 days. 3. Publish a Cryptographic Standards Policy documenting approved algorithms and key management requirements. 4. Conduct NDPA 2023 compliance assessment and register with NDPC as a DCPMI if not already done. 5. Appoint a Data Protection Officer (DPO) as required under the NDPA.

#### NC-010 | Vendor & Third-Party Security | MAJOR NC

| ISO Clause | Domain | Risk Reference | Owner / Target Date |
|---|---|---|---|
| A.5.19 / A.5.20 | Supply Chain | R-006 | GRC Analyst / Legal / CTO | < 45 Days |

**Audit Finding:** Third-party payment processors and cloud service providers are integrated without formal security assessments, security SLAs, or right-to-audit clauses in contracts. No vendor risk register or supplier security review process exists. The CBN Risk-Based Cybersecurity Framework 2024 explicitly requires payment service entities to assess and manage third-party cybersecurity risk.

**Evidence:** Three active payment processor integrations reviewed. None have a documented security assessment on file. Contract review: no security SLAs, data breach notification obligations, or right-to-audit clauses found in any vendor contract reviewed. No vendor risk register maintained. Engineering team confirmed third-party APIs were integrated without security review of documentation.

**Corrective Action:** 1. Establish a vendor risk register listing all critical third parties with risk ratings. 2. Conduct security assessments for all critical payment processor integrations. 3. Update all critical vendor contracts to include: data breach notification obligations (within 72 hours to PayFlow), right-to-audit clause, security SLA, and data protection terms. 4. Require SOC 2 Type II or ISO 27001 attestation from critical vendors annually.

### 5.2 Minor Nonconformities (nc) — Time-Limited Resolution Required

#### NC-011 | Security Metrics & Capacity Monitoring | MINOR NC

| ISO Clause | Domain | Risk Reference | Owner / Target Date |
|---|---|---|---|
| Cl. 9.1 / A.8.6 | Performance Monitoring | R-009 | CISO / IT Admin | < 60 Days |

**Audit Finding:** No security performance metrics or KPIs have been defined. Cloud capacity is not actively monitored. While not a full non-conformity of a specific control, Clause 9.1 requires the organisation to determine what to monitor and measure. Currently, no such determination has been made or documented.

**Evidence:** No security dashboard or KPI tracking tool in use. IT team confirmed capacity alerts are not configured on any cloud resource. No formal measurement plan documented.

**Corrective Action:** 1. Define a set of minimum security KPIs (MFA adoption rate, patch compliance %, open critical vulnerabilities, incident response time). 2. Configure cloud resource alerting thresholds. 3. Report KPIs to management monthly.

#### NC-012 | Clear Desk & Clear Screen Policy | MINOR NC

| ISO Clause | Domain | Risk Reference | Owner / Target Date |
|---|---|---|---|
| A.7.7 | Physical Security | R-009 | IT Admin / HR | < 45 Days |

**Audit Finding:** No clear desk or clear screen policy exists. During the audit, two workstations observed with sensitive documents visible and screens unlocked while staff were away from desks. No automatic screen lock configured on company devices.

**Evidence:** Physical walkthrough of Lagos office: 2 of 7 desks observed with printed documents containing customer names visible. Screen lock timeout not configured — one workstation had been inactive for 18 minutes without locking.

**Corrective Action:** 1. Publish a Clear Desk and Clear Screen Policy. 2. Configure automatic screen lock (5-minute timeout) via MDM or GPO on all company devices. 3. Communicate policy to all staff and include in security awareness training.

#### NC-013 | Asset Inventory | MINOR NC

| ISO Clause | Domain | Risk Reference | Owner / Target Date |
|---|---|---|---|
| A.5.9 | Asset Management | R-009 | IT Admin / GRC Analyst | < 45 Days |

**Audit Finding:** No formal, maintained asset register exists. The Week 1 GRC risk register documents assets at a high level, but there is no operational asset inventory tracking hardware, software, cloud resources, and data assets with ownership, classification, and location.

**Evidence:** IT team confirmed no asset management tool is in use. Hardware asset list was produced ad hoc during the audit — 3 laptops and 1 server could not be immediately accounted for. Cloud resource inventory not formally documented.

**Corrective Action:** 1. Create and maintain a formal asset register covering hardware, software, cloud resources, and data assets. 2. Assign an asset owner to each entry. 3. Review and update quarterly.

#### NC-014 | Backup Testing | MINOR NC

| ISO Clause | Domain | Risk Reference | Owner / Target Date |
|---|---|---|---|
| A.8.13 | Business Continuity | R-007 | IT Admin / DevOps | < 30 Days |

**Audit Finding:** Backups exist for key systems but have not been tested. No documented backup restoration test results were available. ISO 27001 and good practice require that backup integrity and recoverability are periodically verified.

**Evidence:** Backup configuration reviewed: automated backups run daily on primary database and application servers. No restoration test records found. IT administrator confirmed last manual restoration attempt was approximately 8 months ago with no formal record kept.

**Corrective Action:** 1. Conduct a full backup restoration test within 30 days and document the results. 2. Schedule quarterly restoration tests going forward. 3. Define RTO and RPO targets for all critical systems. 4. Store test results as ISMS evidence.

#### NC-015 | Regulatory Contact Register | MINOR NC

| ISO Clause | Domain | Risk Reference | Owner / Target Date |
|---|---|---|---|
| A.5.5 | Compliance & Legal | R-007 | GRC Analyst / Legal | < 45 Days |

**Audit Finding:** No documented register of contacts with relevant regulatory authorities exists. PayFlow has no documented escalation path to the NDPC (for data breaches), CBN (for payment incidents), or Nigerian law enforcement, despite obligations under the NDPA 2023 and the Cybercrimes Act (Amended 2024).

**Evidence:** Legal and compliance records reviewed: no regulatory contact register found. GRC Analyst and CTO interviews confirmed no prior contact with NDPC or CBN security divisions. Under NDPA 2023, data breaches must be reported to the NDPC. The 2024 amendment to the Cybercrimes Act introduces a 72-hour incident reporting requirement.

**Corrective Action:** 1. Compile a regulatory contact register including: NDPC (data breach reporting), CBN (payment system security incidents), Nigerian Cybercrime Advisory Council, and relevant law enforcement contacts. 2. Incorporate regulatory notification procedures into the Incident Response Plan. 3. Review annually.

### 5.3 Opportunities for Improvement (OFI) — Recommended Enhancements

#### OFI-001 | Threat Intelligence | OFI

| ISO Clause | Domain | Risk Reference | Owner / Target Date |
|---|---|---|---|
| A.5.7 | Threat Awareness | R-009 | GRC Analyst / CISO | < 60 Days |

**Audit Finding:** PayFlow currently has no access to threat intelligence relevant to the Nigerian fintech sector. Subscribing to relevant feeds would enhance the quality of risk assessments and ensure awareness of emerging threats targeting payment processors in the region.

**Evidence:** No threat intelligence subscriptions or feeds in use. Staff interviews confirmed no awareness of active threat campaigns targeting Nigerian fintech companies.

**Corrective Action:** Recommended: Subscribe to FS-ISAC (Financial Services Information Sharing and Analysis Center), CERT-NG alerts, and CBN cybersecurity advisories. Integrate threat intelligence into quarterly risk review process.

#### OFI-002 | Secure SDLC & Coding Standards | OFI

| ISO Clause | Domain | Risk Reference | Owner / Target Date |
|---|---|---|---|
| A.8.25 / A.8.28 | Development Security | R-005 | Engineering Lead | < 60 Days |

**Audit Finding:** While the CI/CD pipeline exists and is functional, no security tooling is integrated into the development pipeline. Introducing SAST, DAST, and dependency scanning would proactively reduce vulnerability introduction into production code.

**Evidence:** CI/CD pipeline reviewed (GitHub Actions). No SAST, DAST, or dependency scanning jobs found. Code review is conducted informally — no mandatory review process enforced via branch protection rules.

**Corrective Action:** Recommended: Integrate a SAST tool (e.g., Semgrep, SonarQube) and dependency scanner (e.g., Snyk, Dependabot) into the CI/CD pipeline. Enforce mandatory code review via GitHub branch protection rules. Prioritise OWASP Top 10 vulnerability coverage.

#### OFI-003 | Security Community Engagement | OFI

| ISO Clause | Domain | Risk Reference | Owner / Target Date |
|---|---|---|---|
| A.5.6 | Continuous Improvement | R-009 | GRC Analyst / CEO | < 90 Days |

**Audit Finding:** PayFlow does not currently engage with any information security communities, industry groups, or peer networks. For a fintech operating in Nigeria's rapidly evolving regulatory environment, participation in such forums would improve threat awareness and compliance intelligence.

**Evidence:** No memberships or subscriptions to industry bodies found. No staff participation in security conferences or forums documented.

**Corrective Action:** Recommended: Engage with Nigeria's fintech security community via bodies such as FinTech Nigeria, subscribe to NDPC regulatory updates, and nominate a staff member to attend annual cybersecurity forums (e.g., Cybersafe Nigeria, ISACA Nigeria Chapter).

#### OFI-004 | Web Filtering & DNS Security | OFI

| ISO Clause | Domain | Risk Reference | Owner / Target Date |
|---|---|---|---|
| A.8.23 | Endpoint Protection | R-011 | IT Admin / DevOps | < 60 Days |

**Audit Finding:** No DNS-level web filtering is in place. Implementing a DNS security service would reduce the risk of phishing attacks and malware delivery — particularly important given the lack of security awareness training history and the fast-growing workforce.

**Evidence:** No web filtering tool identified in network or endpoint review. Staff use standard ISP DNS resolution with no threat-blocking layer.

**Corrective Action:** Recommended: Deploy a DNS-based security service (e.g., Cloudflare Gateway, Cisco Umbrella) to block known malicious domains, phishing sites, and command-and-control infrastructure across all company devices and Wi-Fi.

## 6. Corrective Action Register

The table below consolidates all findings into a corrective action register. This register must be reviewed weekly by the CISO and GRC Analyst, with status updates reported to management monthly. Each item must be closed with documented evidence before it can be considered resolved.

| NC ID | Area | Type | Root Cause Category | Owner | Target Date |
|---|---|---|---|---|---|
| NC001 | ISMS Scope & Establishment | MAJOR NC | Governance Gap — No ISMS established | CEO / CISO | < 30 Days |
| NC002 | Risk Treatment Plan | MAJOR NC | Governance Gap — No ISMS established | GRC Analyst / CISO | < 30 Days |
| NC003 | Environment Separation | MAJOR NC | Process Gap — No environment separation | CTO / DevOps Lead | < 1 Week |
| NC004 | Multi-Factor Authentication | MAJOR NC | Technical Gap — MFA not enforced | IT Admin / CISO | < 7 Days |
| NC005 | Secrets & Credential Management | MAJOR NC | Technical Gap — Secrets management absent | Engineering Lead / DevOps | Immediate |
| NC006 | Logging & Security Monitoring | MAJOR NC | Technical Gap — No logging/SIEM | DevOps / IT Admin | < 30 Days |
| NC007 | Incident Response Plan | MAJOR NC | Process Gap — No incident response process | CISO / GRC Analyst | < 30 Days |
| NC008 | Security Awareness Training | MAJOR NC | People Gap — No security training programme | HR / GRC Analyst | < 30 Days |
| NC009 | PII Encryption & Data Protection | MAJOR NC | Technical Gap — Encryption not enforced | DevOps / GRC Analyst / Legal | < 7 Days |
| NC010 | Vendor & Third-Party Security | MAJOR NC | Process Gap — Vendor risk management absent | GRC Analyst / Legal / CTO | < 45 Days |
| NC011 | Security Metrics & Capacity Monitoring | MINOR NC | Governance Gap — No KPI framework | CISO / IT Admin | < 60 Days |
| NC012 | Clear Desk & Clear Screen Policy | MINOR NC | Process Gap — No physical security policy | IT Admin / HR | < 45 Days |
| NC013 | Asset Inventory | MINOR NC | Process Gap — No asset register | IT Admin / GRC Analyst | < 45 Days |
| NC014 | Backup Testing | MINOR NC | Process Gap — Backup testing not scheduled | IT Admin / DevOps | < 30 Days |
| NC015 | Regulatory Contact Register | MINOR NC | Governance Gap — No regulatory contact register | GRC Analyst / Legal | < 45 Days |
| OFI001 | Threat Intelligence | OFI | Enhancement — No blocking nonconformity | GRC Analyst / CISO | < 60 Days |
| OFI002 | Secure SDLC & Coding Standards | OFI | Enhancement — No blocking nonconformity | Engineering Lead | < 60 Days |
| OFI003 | Security Community Engagement | OFI | Enhancement — No blocking nonconformity | GRC Analyst / CEO | < 90 Days |
| OFI004 | Web Filtering & DNS Security | OFI | Enhancement — No blocking nonconformity | IT Admin / DevOps | < 60 Days |

## 7. Regulatory & Multi-Framework Alignment

Several audit findings extend beyond ISO 27001 nonconformities and represent gaps against Nigeria's specific regulatory framework for fintech and data processing entities. The table below cross-references key findings with applicable Nigerian regulations and international frameworks.

| Regulation / Framework | Audit Findings Intersection | Required Action |
|---|---|---|
| NDPA 2023 / GAID 2025 (Nigeria Data Protection Act) | NC-009: Unencrypted PII — violates NDPA requirement for technical measures proportionate to data sensitivity. PayFlow likely qualifies as a DCPMI and must register with the NDPC. GAID 2025 specifies documentation standards and data subject request timelines. | Register with NDPC as a DCPMI immediately (registration deadline was Oct 2024 — late fee applies). Appoint a Data Protection Officer. Conduct a Data Protection Impact Assessment (DPIA). Ensure all PII is encrypted at rest and in transit. |
| CBN Risk-Based Cybersecurity Framework 2024 (Payment Service Banks) | NC-005: Unmanaged credentials; NC-006: No monitoring; NC-010: No vendor risk management. The CBN framework explicitly requires payment entities to manage third-party cybersecurity risk and maintain logging and monitoring capabilities. | Conduct a CBN framework gap assessment. Implement logging and monitoring (NC-006 corrective action). Establish vendor risk management (NC-010 corrective action). Ensure all payment system integrations are assessed against CBN guidelines. |
| Nigeria Cybercrimes Act (Amended 2024) 72-Hour Incident Reporting | NC-007: No IRP means the 72-hour incident notification requirement cannot be met. The 2024 amendment expanded the scope of cybercrime definitions and enhanced requirements for incident reporting to Nigerian authorities. | Incorporate the 72-hour notification procedure into the Incident Response Plan (NC-007 corrective action). Identify the correct reporting authority (Nigerian Cybercrime Advisory Council / relevant agency). Designate a staff member responsible for regulatory notification. |
| PCI DSS v4.0 (Payment Card Industry Data Security Standard) | PayFlow processes card payments and must comply with PCI DSS. This audit did not conduct a full PCI DSS assessment, but findings in access control (NC-003, NC-004), logging (NC-006), and encryption (NC-009) represent likely PCI DSS violations. | Conduct a dedicated PCI DSS gap assessment as a priority. The GRC programme's ISO 27001 work will significantly support PCI DSS compliance but does not replace it. Engage a Qualified Security Assessor (QSA) for formal PCI DSS assessment. |

## 8. Audit Conclusion

| Item | Detail |
|---|---|
| Overall ISMS Maturity Rating | Level 1 — Initial / Ad Hoc (out of 5). Controls are reactive and undocumented. No ISMS is formally established. Security is reliant on individual effort rather than systematic process. |
| Certification Readiness | NOT READY for ISO 27001:2022 certification. 10 Major Nonconformities must be fully resolved and evidenced before Stage 1 documentation audit can proceed. |
| Audit Conclusion | PayFlow demonstrates a genuine commitment to establishing an ISMS through this GRC programme. The appointment of a GRC Analyst, the production of risk documentation, and the drafting of security policies are positive indicators. However, the concentration of Major NCs in foundational areas (governance, access control, logging, incident response, training) means significant work remains before certification is achievable. |
| Estimated Certification Readiness | 6–9 months from the date of this report, provided corrective actions are pursued with executive support and adequate resources. |
| Auditor Statement | This audit was conducted objectively based on document review, technical observation, and staff interviews. All findings are supported by evidence referenced in the individual finding records. This report is submitted to PayFlow management for review and corrective action assignment. |

## 9. Audit Sign-Off

By signing below, the relevant parties confirm they have reviewed this audit report and accepted the findings and corrective action obligations.

| Role | Name | Signature / Date |
|---|---|---|
| Lead Auditor (GRC Analyst) | | |
| Chief Information Security Officer (CISO) | | |
| Chief Technology Officer (CTO) | | |
| Chief Executive Officer (CEO) | | |
