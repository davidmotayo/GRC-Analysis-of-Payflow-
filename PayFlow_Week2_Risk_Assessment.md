# PAYFLOW FINTECH
**GRC Program — Week 2 Deliverable**

## 1. Executive Summary

This document constitutes the Week 2 deliverable of PayFlow's GRC program. Building on the 12 risks and 13 assets identified in Week 1, this assessment performs formal risk scoring against a qualitative 5×5 risk matrix.

## 2. Risk Scoring Methodology

Risk scoring follows the standard qualitative formula:

> **Risk Score = Likelihood (L) × Impact (I)**

Both Likelihood and Impact are rated on a scale of 1 to 5. The resulting score ranges from 1 (minimal risk) to 25 (maximum risk), mapped to four risk levels as defined in the legend below.

### 2.1 Likelihood Scale

| Score | Label | Likelihood Criteria — PayFlow Context |
|---|---|---|
| 5 | Almost Certain | Expected to occur in most circumstances — active exploitation observed or near-certain (e.g., confirmed exposed credential) |
| 4 | Likely | Will probably occur — known vulnerability with available exploit or existing history at PayFlow |
| 3 | Possible | Could occur at some point — vulnerability exists, not yet exploited but realistic within a year |
| 2 | Unlikely | Unlikely to occur — requires skill or opportunity not easily accessible to threat actors |
| 1 | Rare | May only occur under exceptional circumstances — theoretical or highly targeted attack |

### 2.2 Impact Scale

| Score | Label | Impact Criteria — PayFlow Context |
|---|---|---|
| 5 | Catastrophic | Complete system compromise, mass data breach, regulatory shutdown, total loss of investor confidence |
| 4 | Major | Significant data breach or financial loss, major service outage, regulatory investigation, serious reputational harm |
| 3 | Moderate | Partial data exposure, limited service disruption, moderate financial loss, customer complaints |
| 2 | Minor | Minimal data impact, short-lived disruption, minor financial cost, limited reputational effect |
| 1 | Negligible | No meaningful operational impact, recoverable in hours with minimal cost |

### 2.3 Risk Level Legend

| Score Range | Risk Level | Action Required | Governance Note |
|---|---|---|---|
| 20 – 25 | CRITICAL | Immediate action required — escalate to leadership. | Immediate action required. Escalate to executive leadership. Treat before proceeding with partnerships or audits. |
| 12 – 19 | HIGH | Remediate within 30 days. | Remediate within 30 days. Assign accountable owner. Include in quarterly board reporting. |
| 6 – 11 | MEDIUM | Remediate within 90 days. | Remediate within 90 days. Monitor progress monthly. Acceptable to accept temporarily with documented justification. |
| 1 – 5 | LOW | Monitor annually. | Monitor annually. Accept with risk register notation. No immediate action required. |

## 3. Risk Scoring — Detailed Assessment

Each risk from the Week 1 register has been scored for Likelihood and Impact.

| Risk ID | Risk Name | Category | L | I | Score | Level | Scoring Justification |
|---|---|---|---|---|---|---|---|
| R-001 | API Key / Credential Exposure | Technical | 5 | 5 | 25 | CRITICAL | Confirmed incident: API key publicly exposed on GitHub. No secrets management tool in place. Developers have direct repo write access. High exploitability with critical financial system reach. |
| R-002 | PII & Financial Data Unencrypted | Data | 4 | 5 | 20 | CRITICAL | PII and financial data stored without consistent encryption. Cloud buckets have no enforced access policy. Data breach would trigger regulatory penalties and destroy investor confidence. |
| R-003 | Unrestricted Production Access | Access | 4 | 5 | 20 | CRITICAL | All developers have broad production access with no RBAC. No audit logs of production changes. A single compromised developer account grants full system control. |
| R-004 | Inconsistent MFA on Admin Accounts | Access | 4 | 4 | 16 | HIGH | MFA enabled on some admin accounts only. Admin credentials are high-value targets for credential stuffing. Inconsistent enforcement means one weak account compromises the entire admin plane. |
| R-005 | Unsecured Payment APIs | Technical | 3 | 5 | 15 | HIGH | Backend APIs process live financial transactions with no documented security controls, no OAuth enforcement, and no scheduled penetration testing. Exploitable APIs in fintech carry maximum impact. |
| R-006 | Third-Party / Supply Chain Compromise | Vendor | 3 | 5 | 15 | HIGH | Third-party payment processors integrated with no vendor security assessments. Contract terms do not document security obligations. A supply chain breach propagates directly to PayFlow. |
| R-007 | No Incident Response Plan | Operational | 3 | 5 | 15 | HIGH | No documented incident response plan exists. A ransomware or major breach would result in extended downtime, uncoordinated response, and significant financial loss with no recovery playbook. |
| R-008 | Insider Threat / No Security Training | People | 3 | 4 | 12 | HIGH | Rapid onboarding (8 to 45 staff) with no security briefings. Insider access to production data. Negligent or malicious insiders represent a credible and underappreciated threat. |
| R-009 | No Security Policies / Compliance Gap | Compliance | 5 | 3 | 15 | HIGH | Zero formal security policies. No risk assessments ever conducted. PCI DSS and ISO 27001 partnerships will be blocked without immediate policy and compliance framework implementation. |
| R-010 | Cloud Misconfiguration | Technical | 3 | 4 | 12 | HIGH | Confirmed prior misconfiguration (publicly accessible storage bucket). Inconsistent encryption policy. Cloud sprawl increases misconfiguration probability; impact is data exposure at scale. |
| R-011 | Phishing / Social Engineering | People | 4 | 3 | 12 | HIGH | 45+ employees with no phishing awareness training. Fast growth means many new, untrained staff. Email-borne threats remain the most common initial access vector in financial services. |
| R-012 | Reputational / Investor Risk | Operational | 4 | 3 | 12 | HIGH | Prior API key incident has already triggered investor concern. Without an IR plan and governance, a repeat event could result in partnership withdrawal and loss of funding. |

## 4. Risk Matrix — 5×5 Heat Map

The matrix below visualizes all 12 risks across the two-dimensional likelihood/impact space. Each cell displays the calculated risk score and the IDs of any risks positioned at that coordinate.

| Impact / Likelihood → | L = 1 (Rare) | L = 2 (Unlikely) | L = 3 (Possible) | L = 4 (Likely) | L = 5 (Almost Certain) |
|---|---|---|---|---|---|
| **I = 5 (Catastrophic)** | 5 | 10 | 15 — R-005, R-006, R-007 | 20 — R-002, R-003 | 25 — R-001 |
| **I = 4 (Major)** | 4 | 8 | 12 — R-008, R-010 | 16 — R-004 | 20 |
| **I = 3 (Moderate)** | 3 | 6 | 9 | 12 — R-011, R-012 | 15 — R-009 |
| **I = 2 (Minor)** | 2 | 4 | 6 | 8 | 10 |
| **I = 1 (Negligible)** | 1 | 2 | 3 | 4 | 5 |

PayFlow's risk population is heavily clustered in the top-right, confirming the need for immediate governance intervention.

## 5. Risk Summary

| Level | Count | % Total | Risk IDs |
|---|---|---|---|
| CRITICAL | 3 | 25% | R-001, R-002, R-003 |
| HIGH | 9 | 75% | R-004, R-005, R-006, R-007, R-008, R-009, R-010, R-011, R-012 |
| MEDIUM | 0 | 0% | None |
| LOW | 0 | 0% | None identified |
| **TOTAL** | **12** | **100%** | R-001 through R-012 |

**Key finding:** No risks were scored LOW. The absence of even a single low-risk finding reflects a security environment that is almost entirely uncontrolled.
