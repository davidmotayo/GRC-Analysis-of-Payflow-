# Executive Compliance & Security Report

## 1. Executive Summary

This report presents the findings of PayFlow Fintech Nigeria Ltd.'s first structured Information Security Governance, Risk, and Compliance (GRC) programme. It is prepared for the Board of Directors and senior leadership as a consolidated view of the company's current security posture, compliance status, identified risks, and the remediation roadmap required to achieve ISO/IEC 27001:2022 certification and full regulatory compliance under applicable Nigerian law.

The programme was conducted over seven structured weeks, producing six formal deliverables: a Risk Register, Risk Assessment, Security Policies, an ISO 27001 Compliance Checklist, an Internal Audit Findings Report, and a Risk Treatment Plan with Statement of Applicability. This report synthesises all findings into an executive-ready format.

## 2. Risk Posture Summary

PayFlow's risk posture, as established through Weeks 1–2 of the programme and validated by the Week 5 internal audit, reflects an organisation at Level 1 security maturity — where controls are reactive, largely undocumented, and reliant on individual effort rather than systematic process.

| Risk ID | Risk Name | Score | Level | Treatment | Residual | Audit NC |
|---|---|---|---|---|---|---|
| R-001 | API Key / Credential Exposure | 25 | CRITICAL | MITIGATE | LOW | NC-005 |
| R-002 | PII & Financial Data Unencrypted | 20 | CRITICAL | MITIGATE | MEDIUM | NC-009 |
| R-003 | Unrestricted Production Access | 20 | CRITICAL | MITIGATE | MEDIUM | NC-003 |
| R-004 | Inconsistent MFA on Admin Accounts | 16 | HIGH | MITIGATE | LOW | NC-004 |
| R-005 | Unsecured Payment APIs | 15 | HIGH | MITIGATE | MEDIUM | OFI-002 |
| R-006 | Third-Party / Supply Chain Compromise | 15 | HIGH | MITIGATE + TRANSFER | MEDIUM | NC-010 |
| R-007 | No Incident Response Plan | 15 | HIGH | MITIGATE | MEDIUM | NC-007 |
| R-008 | Insider Threat / No Security Training | 12 | HIGH | MITIGATE | MEDIUM | NC-008 |
| R-009 | No Formal ISMS / Compliance Governance | 15 | HIGH | MITIGATE | MEDIUM | NC-001/002 |
| R-010 | Cloud Misconfiguration | 12 | HIGH | MITIGATE | LOW | NC-006 |
| R-011 | Phishing / Social Engineering | 12 | HIGH | MITIGATE | MEDIUM | OFI-004 |
| R-012 | Reputational / Investor Risk | 12 | HIGH | ACCEPT + MITIGATE | MEDIUM | — |

### 2.1 Risk Distribution

| Risk Level | Count | % of Total |
|---|---|---|
| CRITICAL | 3 | 25% |
| HIGH | 9 | 75% |
| MEDIUM | 0 | 0% |
| LOW | 0 | 0% |

## 3. ISO/IEC 27001:2022 Compliance Status

The Week 4 compliance checklist assessed all 118 applicable ISO/IEC 27001:2022 requirements — 25 clause requirements across Clauses 4–10 (ISMS Core) plus all 93 Annex A controls across the four 2022 themes (A.5–A.8). The distribution below represents PayFlow's current compliance posture — the baseline against which progress will be measured.

| Status | Count | % of Total | Interpretation |
|---|---|---|---|
| COMPLIANT | 0 | 0% | No control is fully implemented and evidenced. This reflects the absence of an ISMS prior to this programme. |
| PARTIAL | 35 | 30% | Controls where initial work exists — Password Policy (POL-SEC-001), Access Control Policy (POL-SEC-002), Risk Register — but technical enforcement is not yet complete. |
| NON-COMPLIANT | 80 | 68% | Controls that are entirely absent. The primary target of the Risk Treatment Plan (RTP-001) and the implementation roadmap. |
| EXCLUDED (N/A) | 3 | — | A.7.6, A.7.12, A.8.30 — not applicable to PayFlow's cloud-first, in-house development model. Justified and documented in SOA-001. |

### 3.1 Compliance by ISO 27001 Domain

| Domain | Controls | Key Gap | Priority | Lead Deliverable |
|---|---|---|---|---|
| Clauses 4–10 (ISMS Core) | 25 | No ISMS established; no SoA, no risk treatment plan prior to this programme | CRITICAL RISK | RTP-001 / SOA-001 |
| A.5 — Organisational Controls | 37 | No InfoSec policy, no asset register, no IRP, no vendor contracts — 33 of 37 fully absent | CRITICAL RISK | AUD-RPT001 |
| A.6 — People Controls | 8 | Zero security training for all 45 staff; no background screening; no NDAs with vendors | CRITICAL RISK | AUD-RPT001 |
| A.7 — Physical Controls | 14 | No clear desk policy; no device encryption confirmed; no asset register | MEDIUM RISK | GRC-CHK-001 |
| A.8 — Technological Controls | 34 | No SIEM; no MFA enforcement; no env. separation; no secrets management; no vulnerability scanning | CRITICAL RISK | RTP-001 |

## 4. Internal Audit Findings Summary

The Week 5 internal audit — PayFlow's first formal ISMS audit — was conducted against ISO/IEC 27001:2022. Of 19 total findings, 10 are Major Nonconformities that directly block certification. The table below summarises each finding for board visibility.

| NC ID | Domain | Type | Finding Summary | Owner | Target |
|---|---|---|---|---|---|
| NC001 | ISMS Governance | MAJOR NC | No ISMS established. No scope statement or top-management approved Information Security Policy. | CEO/CISO | < 30 Days |
| NC002 | Risk Management | MAJOR NC | No risk treatment plan or Statement of Applicability existed prior to this programme. | CISO | < 30 Days |
| NC003 | Access Control | MAJOR NC | 11 of 12 developers have unrestricted production access. No environment separation. | CTO | < 7 Days |
| NC004 | Identity Management | MAJOR NC | 28 of 45 accounts (62%) lack MFA. 4 of 12 admin accounts without MFA. | IT Admin | < 7 Days |
| NC005 | Secrets Hygiene | MAJOR NC | Hardcoded credentials in 2 active repos. No secrets manager. Prior API key incident unresolved. | Eng. Lead | Immediate |
| NC006 | Monitoring | MAJOR NC | No SIEM. CloudTrail not forwarded. Only 2 of 8 storage buckets have access logs enabled. | DevOps | < 30 Days |
| NC007 | Incident Response | MAJOR NC | No Incident Response Plan. Prior incident handled via Slack. 72-hr reporting impossible. | CISO | < 30 Days |
| NC008 | People Security | MAJOR NC | Zero security training records for all 45 staff. Onboarding has no security briefing. | HR | < 30 Days |
| NC009 | Data Protection | MAJOR NC | 3 of 8 cloud buckets contain unencrypted PII. NDPA 2023 non-compliance. | DevOps | < 7 Days |
| NC010 | Vendor Risk | MAJOR NC | No security assessments for payment processor integrations. No security SLAs in contracts. | Legal/CTO | < 45 Days |
| NC011 | Performance | MINOR NC | No security KPIs or metrics framework. No cloud capacity alerting. | CISO | < 60 Days |
| NC012 | Physical Security | MINOR NC | No clear desk policy. Unattended screens observed unlocked during audit walkthrough. | IT Admin | < 45 Days |
| NC013 | Asset Management | MINOR NC | No formal asset register. 3 laptops unaccounted for during audit. | IT Admin | < 45 Days |
| NC014 | Business Continuity | MINOR NC | Backups exist but last restoration test was 8+ months ago with no formal record. | IT Admin | < 30 Days |
| NC015 | Compliance | MINOR NC | No regulatory contact register for NDPC, CBN, or law enforcement escalation. | Legal | < 45 Days |

### 4.1 Audit Conclusion

**Overall ISMS Maturity Rating: Level 1 — Initial / Ad Hoc**

Controls are reactive and undocumented. Security is reliant on individual effort rather than systematic process. PayFlow is **NOT READY** for ISO/IEC 27001:2022 certification. All 10 Major Nonconformities must be fully resolved and supported by documented evidence before a Stage 1 documentation audit can proceed. Estimated certification readiness: **6–9 months** from this report date, subject to executive commitment and adequate resource allocation.

## 5. Regulatory Compliance Status

PayFlow operates in Nigeria's fintech sector and is subject to multiple overlapping regulatory obligations. The audit identified gaps that create legal exposure beyond the ISO 27001 certification scope. The table below presents the current compliance rating against each applicable framework.

| Regulation / Framework | Rating | Key Gaps Identified | Required Action & Consequence of Inaction |
|---|---|---|---|
| Nigeria Data Protection Act (NDPA 2023) | NON-COMPLIANT | PII stored unencrypted (NC-009); no DPO appointed; no DPIA conducted; likely DCPMI status unregistered with NDPC. | Register with NDPC as DCPMI immediately; appoint DPO; conduct DPIA; encrypt all PII. Consequence: fines up to ₦1 billion per incident. Precedent: ₦766.2m (Multichoice), $220m (Meta). |
| NDPC General Application & Implementation Directive (GAID 2025) | NON-COMPLIANT | No documented data processing records; no data subject rights procedure; no cross-border transfer safeguards documented. | GAID 2025 specifies documentation standards, consent requirements, and data transfer rules. All must be addressed within the ISMS documentation programme. |
| CBN Risk-Based Cybersecurity Framework 2024 | NON-COMPLIANT | No CISO-signed annual cybersecurity report to CBN (due March 31 annually); no third-party risk management; no logging and monitoring capability. | Implement logging (NC-006), vendor risk management (NC-010), and establish CISO annual reporting process. Consequence: regulatory sanctions from CBN on payment operations. |
| Nigeria Cybercrimes Act (Amended 2024) | NON-COMPLIANT | No Incident Response Plan (NC-007); 72-hour incident reporting impossible without documented process and regulatory contact register. | Develop IRP with 72-hr notification procedure as immediate priority (R-007). Consequence: criminal liability and regulatory sanctions for unreported incidents. |
| PCI DSS v4.0 | NON-COMPLIANT | Access control gaps (NC-003, NC-004); no logging (NC-006); unencrypted data (NC-009); no vulnerability management; no Secure SDLC. | Dedicated PCI DSS gap assessment required alongside ISO 27001 programme. ISO 27001 controls overlap significantly. Engage a Qualified Security Assessor (QSA). |
| ISO/IEC 27001:2022 | NOT READY | 10 Major NCs block certification. 91% of controls non-compliant or absent. No ISMS formally established. | Complete all Major NC corrective actions. Produce full ISMS documentation set. Target Stage 1 audit in 6 months. |

## 6. Risk Treatment Progress

The Risk Treatment Plan (RTP-001) produced in Week 6 defines the treatment for all 12 risks. The following table shows current implementation status against the planned timeline. This tracker should be presented to the board quarterly.

| Risk ID | Risk Name | Treatment | Target | Status | Corrective Action |
|---|---|---|---|---|---|
| R-001 | API Key / Credential Exposure | MITIGATE | 7 Days | NOT STARTED | Deploy secrets manager; rotate all keys; pre-commit scanning |
| R-002 | PII & Financial Data Unencrypted | MITIGATE | 7 Days | NOT STARTED | AES-256 encryption; DPIA; NDPC registration; DPO appointment |
| R-003 | Unrestricted Production Access | MITIGATE | 30 Days | NOT STARTED | Revoke prod access; implement RBAC; deploy PAM tooling |
| R-004 | Inconsistent MFA | MITIGATE | 7 Days | NOT STARTED | Enforce MFA via Conditional Access for all 45 accounts |
| R-005 | Unsecured Payment APIs | MITIGATE | 60 Days | NOT STARTED | SAST/DAST in CI/CD; OAuth on all APIs; quarterly pentest |
| R-006 | Third-Party / Supply Chain | MITIGATE + TRANSFER | 45 Days | NOT STARTED | Vendor risk register; contract review; cyber insurance |
| R-007 | No Incident Response Plan | MITIGATE | 30 Days | NOT STARTED | Develop IRP; assign IR team; tabletop exercise; 72-hr procedure |
| R-008 | Insider Threat / No Training | MITIGATE | 30 Days | NOT STARTED | Mandatory training for all 45 staff; phishing simulation |
| R-009 | No Formal ISMS | MITIGATE | 30 Days | IN PROGRESS | InfoSec Policy; ISMS scope; RACI; this GRC programme |
| R-010 | Cloud Misconfiguration | MITIGATE | 30 Days | NOT STARTED | CSPM tool; CloudTrail; SIEM; CIS benchmark baselines |
| R-011 | Phishing / Social Engineering | MITIGATE | 45 Days | NOT STARTED | Awareness training; DNS filtering; EDR; email gateway |
| R-012 | Reputational / Investor Risk | ACCEPT + MITIGATE | 60 Days | PLANNED | IRP comms protocol; investor security briefing |

## 7. ISO 27001 Certification Roadmap

Based on all programme findings, the following phased roadmap sets out the path from current state (Level 1 maturity) to ISO/IEC 27001:2022 certification. The board is asked to endorse this roadmap and allocate the necessary resources to execute it.

### Phase 1 — Foundation (Months 1–2)
**Key Milestones:**
- All 10 Major NC corrective actions initiated
- MFA enforced for all 45 accounts
- Production access revoked and RBAC implemented
- PII encryption enforced across all cloud storage
- Secrets manager deployed and all keys rotated
- Information Security Policy signed by CEO/CTO
- ISMS scope document published

**Success Criteria:** 0 CRITICAL risks without active corrective action. MFA adoption: 100%. All PII encrypted. IRP published.

### Phase 2 — Core Controls (Months 2–4)
**Key Milestones:**
- SIEM deployed with alerting rules live
- IRP tested via tabletop exercise
- Security awareness training: all 45 staff completed
- Vendor risk assessments completed for all Tier-1 vendors
- SAST/DAST integrated in CI/CD pipeline
- Network segmentation implemented
- NDPA DPIA completed; NDPC registration confirmed

**Success Criteria:** SIEM operational. Training completion 100%. Vendor contracts updated. NDPC registered. DPO appointed.

### Phase 3 — Governance (Months 4–6)
**Key Milestones:**
- Full policy suite published and communicated
- Internal audit programme established (Clause 9.2)
- Management review process active (Clause 9.3)
- Asset register complete and current
- PCI DSS gap assessment completed
- Quarterly access reviews conducted
- CBN annual cybersecurity report filed

**Success Criteria:** All Minor NCs closed. Management review minuted. PCI DSS gap report available. KPI dashboard operational.

### Phase 4 — Certification (Months 7–9)
**Key Milestones:**
- Stage 1 documentation audit (external auditor)
- Stage 1 findings addressed and evidenced
- Stage 2 certification audit (on-site)
- Minor nonconformities from Stage 2 closed
- ISO/IEC 27001:2022 certificate issued

**Success Criteria:** Certificate issued. Zero open Major NCs. Full SoA implemented. Surveillance audit programme in place.

## 8. Recommended Board Actions

The GRC Analyst requests the following decisions and approvals from the Board of Directors to enable progression of the ISMS programme. These are listed in priority order.

| # | Priority | Action Required | Rationale | Target |
|---|---|---|---|---|
| 1 | CRITICAL | Approve and sign the Information Security Policy | This is the foundational document of the ISMS. Without CEO/CTO signature, ISO 27001 certification cannot proceed. It also signals organisational commitment to investors and partners. | Immediate |
| 2 | CRITICAL | Authorise immediate PII encryption and NDPC registration | PayFlow is currently non-compliant with NDPA 2023. Precedent fines reach ₦1 billion per incident. The NDPC registration process must begin immediately to avoid regulatory enforcement. | < 7 Days |
| 3 | CRITICAL | Mandate universal MFA and revoke developer production access | 28 of 45 accounts lack MFA. 11 of 12 developers have unrestricted production access. Both are audit-confirmed CRITICAL risks that can be addressed at near-zero cost within 7 days. | < 7 Days |
| 4 | HIGH | Approve budget for ISMS tooling (SIEM, PAM, CSPM, MDM, Pentest) | The Risk Treatment Plan requires a suite of security tools. Without budget approval, implementation cannot begin. Recommend prioritising: SIEM (AWS Security Hub or equivalent), PAM tooling, and a quarterly penetration testing engagement. | < 30 Days |
| 5 | HIGH | Approve appointment of a Data Protection Officer (DPO) | The NDPA 2023 requires a DPO for organisations processing personal data at scale. PayFlow qualifies as a DCPMI. The DPO must be appointed and registered with the NDPC. | < 30 Days |
| 6 | HIGH | Endorse the ISO 27001 Certification Roadmap | Board endorsement of the 9-month certification roadmap enables the GRC Analyst and CISO to drive remediation with executive authority. This is required before any international payment partnership can proceed. | < 30 Days |
| 7 | MEDIUM | Schedule quarterly ISMS management review meetings | ISO 27001 Clause 9.3 requires top management to review the ISMS periodically. The first management review should be scheduled for Month 3 of the programme. | < 60 Days |
| 8 | MEDIUM | Approve update of all critical vendor contracts | Legal must be instructed to update all payment processor and cloud service provider contracts to include: 72-hr data breach notification, right-to-audit, security SLAs, and NDPA 2023 data processing terms. | < 45 Days |

## 9. Board Acknowledgement

By signing below, the Board acknowledges receipt and review of this Compliance and Security Report, and confirms the decisions made on the Recommended Board Actions in Section 9.

| Role | Name | Signature / Date |
|---|---|---|
| Chief Executive Officer (CEO) | | |
| Chief Technology Officer (CTO) | | |
| Chief Information Security Officer (CISO) | | |
| GRC Analyst (Author) | | |
| Board Member / Non-Executive Director | | |
