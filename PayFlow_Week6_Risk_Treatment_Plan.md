# Risk Treatment Plan

## 1. Executive Summary

This Risk Treatment Plan (RTP) documents the recommended controls and treatment strategies for all twelve (12) risks identified in PayFlow's Week 1 Risk Register and scored in the Week 2 Risk Assessment. The plan is structured to guide PayFlow from its current high-risk posture toward a state of compliance-readiness aligned with ISO/IEC 27001, PCI DSS, and the Nigeria Data Protection Act 2023 (NDPA).

Each risk has been assigned a treatment strategy — Remediate, Mitigate, Transfer, or Accept — along with specific actionable controls, responsible owners, and realistic implementation timelines. Upon full implementation, all CRITICAL risks are expected to reduce to LOW or MEDIUM residual levels, and no HIGH or CRITICAL risk is expected to remain untreated.

The overarching goals of this treatment plan are:

- Eliminate the most critical and immediately exploitable vulnerabilities
- Establish foundational security governance structures and formal policies
- Protect sensitive customer PII and financial data in line with regulatory obligations
- Prepare the organisation for external compliance audits and international partnerships
- Build a culture of security awareness across all departments

## 2. Treatment Strategy Framework

PayFlow's risk treatment decisions are guided by four standard strategies, applied singly or in combination where appropriate. Strategy selection was based on the inherent risk rating, feasibility of control implementation, cost-effectiveness, and alignment with regulatory obligations.

| Strategy | Definition | Risks Assigned |
|---|---|---|
| Remediate | Eliminate the root cause of the risk immediately | R-001 (Exposed API Key) |
| Mitigate | Reduce the likelihood or impact through controls | R-002, R-003, R-004, R-005, R-007, R-008, R-009, R-010, R-011 |
| Mitigate + Transfer | Reduce impact through controls, and shift residual exposure via contract terms or insurance | R-006 (Third-Party / Supply Chain Compromise) |
| Accept + Mitigate | Acknowledge residual reputational exposure while reducing likelihood through governance controls | R-012 (Reputational / Investor Risk) |

## 3. Risk Treatment Register

The following table details the full risk treatment register for PayFlow. For each identified risk, the plan specifies the treatment strategy, recommended controls, accountable owner, implementation timeline, and expected residual risk rating after controls are applied. Risk IDs, owners, and timelines are aligned with the master risk register (Week 1/2) and consolidated in the Week 8 Security Governance Plan.

### R-001 — Exposed API key on public GitHub repository
- **Inherent Rating:** CRITICAL (Score: 25)
- **Treatment Strategy:** Remediate
- **Owner:** Engineering Lead / DevOps
- **Timeline:** 0–7 days
- **Residual Rating:** LOW
- **Controls & Recommended Actions:**
  1. Immediately rotate all exposed API keys and secrets
  2. Implement pre-commit hooks (e.g., git-secrets, TruffleHog) to prevent future leaks
  3. Adopt a secrets management solution (e.g., HashiCorp Vault, AWS Secrets Manager)
  4. Enable GitHub Advanced Security / secret scanning alerts
  5. Conduct developer training on secure credential handling

### R-002 — PII and financial data unencrypted / inadequately protected
- **Inherent Rating:** CRITICAL (Score: 20)
- **Treatment Strategy:** Mitigate
- **Owner:** DevOps / GRC Analyst / Legal
- **Timeline:** 7 days
- **Residual Rating:** MEDIUM
- **Controls & Recommended Actions:**
  6. Conduct a PII data mapping exercise to classify and locate all PII assets
  7. Enable AES-256 encryption on all databases and analytical read-replicas holding PII
  8. Implement data minimization — retain only necessary PII fields
  9. Tokenize or mask financial data where full values are not required
  10. Conduct a Data Protection Impact Assessment (DPIA) and register with the NDPC as a DCPMI
  11. Appoint a Data Protection Officer (DPO)
  12. Define and enforce a data retention and disposal policy aligned with NDPA 2023 obligations

### R-003 — Unrestricted developer access to production systems
- **Inherent Rating:** CRITICAL (Score: 20)
- **Treatment Strategy:** Mitigate
- **Owner:** CTO / DevOps Lead
- **Timeline:** 30 days
- **Residual Rating:** MEDIUM
- **Controls & Recommended Actions:**
  13. Define and document roles: Admin, Developer, Senior Developer, Analyst, Read-Only
  14. Implement least-privilege principle across all cloud and system accounts
  15. Revoke standing developer access to production; provision via separate AWS/GCP IAM roles per environment (dev, staging, prod)
  16. Enforce time-limited, just-in-time production access with change approval
  17. Review and recertify privileged access quarterly

### R-004 — Inconsistent MFA enforcement across user accounts
- **Inherent Rating:** HIGH (Score: 16)
- **Treatment Strategy:** Mitigate
- **Owner:** IT Administrator
- **Timeline:** 7 days
- **Residual Rating:** LOW
- **Controls & Recommended Actions:**
  18. Enforce MFA for all 45 accounts — administrative and standard, no exceptions
  19. Use an Identity Provider (IdP) such as Okta or Google Workspace SSO
  20. Set Conditional Access policies to block logins without MFA
  21. Prioritise hardware-key MFA for privileged/admin accounts
  22. Monitor and alert on MFA bypass attempts

### R-005 — Unsecured payment APIs / no security testing in the SDLC
- **Inherent Rating:** HIGH (Score: 15)
- **Treatment Strategy:** Mitigate
- **Owner:** Engineering Lead
- **Timeline:** 60 days
- **Residual Rating:** MEDIUM
- **Controls & Recommended Actions:**
  23. Integrate Static Application Security Testing (SAST) into the CI/CD pipeline
  24. Perform Dynamic Application Security Testing (DAST) before each major release
  25. Implement mandatory code review with security sign-off for production deployments
  26. Enforce OAuth on all payment API endpoints
  27. Conduct an annual penetration test by an external provider
  28. Adopt OWASP ASVS as a baseline security standard for APIs

### R-006 — Third-party / supply chain compromise
- **Inherent Rating:** HIGH (Score: 15)
- **Treatment Strategy:** Mitigate + Transfer
- **Owner:** Legal / CTO
- **Timeline:** 45 days
- **Residual Rating:** MEDIUM
- **Controls & Recommended Actions:**
  29. Establish a vendor risk register listing all critical third parties with risk ratings
  30. Conduct security assessments for all critical payment processor integrations
  31. Update all critical vendor contracts to include: 72-hour data breach notification obligations, a right-to-audit clause, and a security SLA
  32. Require SOC 2 Type II or ISO 27001 attestation from critical vendors annually
  33. Evaluate cyber insurance coverage to transfer residual financial exposure from a vendor-side breach

### R-007 — No documented incident response (IR) plan
- **Inherent Rating:** HIGH (Score: 15)
- **Treatment Strategy:** Mitigate
- **Owner:** CISO
- **Timeline:** 30 days
- **Residual Rating:** MEDIUM
- **Controls & Recommended Actions:**
  34. Develop and publish a formal Incident Response Plan (IRP) covering preparation, detection, containment, eradication, recovery, and lessons learned
  35. Define incident severity levels (P1–P4) and escalation procedures
  36. Assign IR roles: Incident Commander, Communications Lead, Technical Lead
  37. Document the 72-hour regulatory notification procedure required under the Nigeria Cybercrimes Act (Amended 2024) and NDPA 2023
  38. Conduct a tabletop IR exercise within 60 days of IRP publication
  39. Integrate the IR plan with communication obligations to partners, investors, and regulators

### R-008 — Insider threat / no security awareness training
- **Inherent Rating:** HIGH (Score: 12)
- **Treatment Strategy:** Mitigate
- **Owner:** HR / GRC Analyst
- **Timeline:** 30 days
- **Residual Rating:** MEDIUM
- **Controls & Recommended Actions:**
  40. Create a mandatory security onboarding checklist for all new hires
  41. Deliver security awareness training within the first week of employment; mandatory completion within 30 days for all 45 existing staff
  42. Require all employees to sign an Acceptable Use Policy (AUP)
  43. Include social engineering / phishing awareness modules
  44. Run quarterly refresher training and maintain completion records for audit evidence

### R-009 — No formal ISMS / compliance governance
- **Inherent Rating:** HIGH (Score: 15)
- **Treatment Strategy:** Mitigate
- **Owner:** CISO / GRC Analyst
- **Timeline:** 30 days
- **Residual Rating:** MEDIUM
- **Controls & Recommended Actions:**
  45. Draft and obtain CEO/CTO sign-off on a formal Information Security Policy and ISMS scope statement
  46. Draft and approve the core security policy suite (Password, Access Control, Acceptable Use, Data Classification policies) and publish to all staff
  47. Implement an annual formal risk assessment (ISO/IEC 27005-aligned methodology); maintain a live risk register updated quarterly
  48. Appoint a named Risk Owner for each identified risk
  49. Map all policies and treatment controls to ISO/IEC 27001 Annex A for audit readiness
  50. Review and update all policies annually or after significant organisational change

### R-010 — Cloud misconfiguration / inconsistent encryption on storage
- **Inherent Rating:** HIGH (Score: 12)
- **Treatment Strategy:** Mitigate
- **Owner:** DevOps / Cloud Team
- **Timeline:** 30 days
- **Residual Rating:** LOW
- **Controls & Recommended Actions:**
  51. Define and publish a Cryptographic Standards Policy covering data at rest and in transit
  52. Enable server-side encryption (AES-256) on all cloud storage buckets
  53. Enforce TLS 1.2+ on all API endpoints and internal communications
  54. Audit existing storage buckets and remediate any unencrypted assets
  55. Deploy a CSPM tool and CIS Benchmark configuration baselines
  56. Align with PCI DSS Requirement 3 (data at rest) and Requirement 4 (data in transit)

### R-011 — Phishing / social engineering
- **Inherent Rating:** HIGH (Score: 12)
- **Treatment Strategy:** Mitigate
- **Owner:** IT Administrator
- **Timeline:** 45 days
- **Residual Rating:** MEDIUM
- **Controls & Recommended Actions:**
  57. Deploy a DNS-based web filtering service (e.g., Cloudflare Gateway, Cisco Umbrella) across all company devices and Wi-Fi
  58. Deploy endpoint detection and response (EDR) and a secure email gateway
  59. Run monthly phishing simulations with results reported to the GRC Analyst and HR
  60. Fold phishing recognition into the mandatory security awareness training (R-008)
  61. Trigger targeted follow-up training for staff who fail simulations

### R-012 — Reputational / investor risk
- **Inherent Rating:** HIGH (Score: 12)
- **Treatment Strategy:** Accept + Mitigate
- **Owner:** CEO / Legal
- **Timeline:** 60 days
- **Residual Rating:** MEDIUM
- **Controls & Recommended Actions:**
  62. Publish an investor/partner communications protocol as part of the Incident Response Plan (R-007)
  63. Brief investors and key partners on the GRC programme and remediation roadmap to rebuild confidence following the prior API key exposure
  64. Report ISMS progress (KPIs, corrective action closure) to the board quarterly
  65. Accept residual reputational exposure within board-defined tolerance once governance and technical controls (R-001–R-011) are operating effectively

## 4. Residual Risk Summary

Following full implementation of the recommended controls, the residual risk distribution is projected as follows. The organisation will have successfully eliminated all CRITICAL and HIGH residual risks, with nine MEDIUM risks remaining pending longer-term programme maturity.

| Residual Risk Level | Count | Risk IDs |
|---|---|---|
| LOW | 3 | R-001, R-004, R-010 |
| MEDIUM | 9 | R-002, R-003, R-005, R-006, R-007, R-008, R-009, R-011, R-012 |
| HIGH | 0 | None — all HIGH/CRITICAL risks treated to MEDIUM or below |
| CRITICAL | 0 | None |

*Note: MEDIUM residual risks reflect controls whose full effectiveness depends on ongoing programme maturity — incident response practice, secure SDLC adoption, vendor governance, and phishing resilience — rather than a one-time fix. These will be revisited in subsequent review cycles as the programme matures.*

## 5. Priority Quick Wins (Immediate Action Required)

The following five actions are flagged as immediate priorities due to their high impact, low implementation effort, and direct relevance to investor concerns and upcoming partner due diligence. These should be actioned within the first two weeks of plan adoption.

| Priority | Action | Risk(s) Addressed | Effort | Impact |
|---|---|---|---|---|
| 1 | Rotate exposed API key and enable secret scanning | R-001 | Low | Critical |
| 2 | Enforce MFA for all accounts | R-004 | Low | High |
| 3 | Enable encryption on all cloud storage buckets | R-010 | Low | High |
| 4 | Revoke excessive developer production access | R-003 | Low | High |
| 5 | Initiate security awareness training for all staff | R-008 | Low | Medium |

## 6. Implementation Roadmap

The roadmap below organises the treatment actions into four delivery phases over an eight-week period, followed by ongoing continuous improvement activities. Phase sequencing prioritises critical vulnerability elimination before process formalisation.

| Phase | Timeframe | Key Actions | Risks Addressed |
|---|---|---|---|
| Phase 1 | Weeks 1–2 | Rotate API keys • Enforce MFA • Enable bucket encryption • Revoke excessive developer access | R-001, R-003, R-004, R-010 |
| Phase 2 | Weeks 3–4 | Draft and publish core security policies • Begin RBAC implementation • Launch IR plan development • Start security onboarding programme | R-007, R-008, R-009 |
| Phase 3 | Weeks 5–6 | Formalise the risk register • Complete PII data mapping and DPIA • Implement tokenization • Conduct tabletop IR exercise • Stand up vendor risk register | R-002, R-006, R-007 |
| Phase 4 | Weeks 7–8 | Integrate SAST/DAST into CI/CD • Conduct code review gates • Engage external penetration testing provider • Deploy DNS filtering/EDR • Publish investor communications protocol | R-005, R-011, R-012 |
| Ongoing | Quarterly | Recertify access • Refresh security training • Update risk register • Review and update policies • Re-run phishing simulations | All risks |

## 7. Roles & Responsibilities

Effective risk treatment requires clear ownership. The following roles bear primary responsibility for coordinating and executing treatment activities:

- **GRC Analyst** — Plan coordination, policy drafting, compliance mapping, progress reporting
- **CISO / Head of Security** — Executive oversight, policy sign-off, vendor engagement
- **DevOps / Engineering Lead** — Technical control implementation (encryption, RBAC, CI/CD security)
- **IT Security Team** — MFA enforcement, access reviews, monitoring configuration
- **HR Department** — Security onboarding programme, training coordination
- **Data Protection Officer** — PII mapping, NDPA 2023 compliance, data retention policy
- **Leadership / Board** — Resource allocation, risk acceptance decisions, partner communications

## 8. Monitoring, Review & Reporting

Implementation of this Risk Treatment Plan is not a one-time activity. The following monitoring and review cadence is recommended to ensure sustained effectiveness:

- **Weekly Status Updates** — GRC Analyst to track progress against milestones and report blockers to CISO
- **Monthly Control Testing** — Validate that implemented controls are operating as intended (e.g., MFA logs, bucket encryption status, access control reviews)
- **Quarterly Risk Register Review** — Reassess risk ratings, update residual risk scores, and identify any new or emerging risks
- **Annual Full Risk Assessment** — Conduct comprehensive organisational risk assessment aligned with ISO/IEC 27001:2022 Clause 6.1.2
- **Post-Incident Review** — Trigger risk register update and control re-evaluation following any security incident

All findings, exceptions, and control gaps identified during monitoring activities shall be formally documented and escalated to leadership through a Risk & Compliance Dashboard.

## 9. Compliance Framework Alignment

The controls recommended in this plan align to the following frameworks and standards. Full control mapping will be completed in the Week 7 compliance reporting deliverable.

- **ISO/IEC 27001:2022** — Annex A controls across all four 2022 themes: A.5 (Organisational Controls, incl. policies and access control), A.6 (People Controls), A.7 (Physical Controls), and A.8 (Technological Controls, incl. operations security and incident management)
- **PCI DSS v4.0** — Requirements 3 (Data Protection), 4 (Encryption in Transit), 7 (Access Control), 8 (Authentication), 12 (Security Policies)
- **NIST Cybersecurity Framework** — Identify, Protect, Detect, Respond, and Recover functions
- **NDPA 2023 (Nigeria Data Protection Act)** — Data subject rights, lawful basis for processing, data retention and disposal, breach notification obligations

## 10. Approval & Sign-Off

This Risk Treatment Plan requires formal approval from the following stakeholders before implementation commences. Approval constitutes commitment to resource allocation and accountability for assigned actions.

| Role | Name | Signature | Date |
|---|---|---|---|
| GRC Analyst (Author) | | | |
| CISO / Head of Security | | | |
| Chief Executive Officer | | | |
