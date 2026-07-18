# ACCESS CONTROL POLICY
**PayFlow Fintech Nigeria Ltd.**

## 1. Purpose

This Access Control Policy defines the principles and mandatory requirements governing how access to PayFlow's information systems, data, applications, and infrastructure is granted, maintained, reviewed, and revoked. It directly addresses risks R-003 (Unrestricted Production Access) and R-004 (Inconsistent MFA) identified as CRITICAL and HIGH respectively in PayFlow's formal risk assessment.

The fundamental principle underpinning this policy is **least privilege**: every user, system, and process must be granted only the minimum level of access necessary to perform their defined function — and no more.

## 2. Scope

This policy applies to:

- All PayFlow employees, contractors, temporary staff, interns, and third-party vendors with any form of system access
- All information systems, cloud platforms, backend APIs, databases, payment processing systems, and internal tools
- All access types: logical (system/application), physical (server room), remote (VPN/SSH), and privileged (admin/root)
- All account types: standard user, privileged/administrator, service account, API account, and shared account

## 3. Access Control Principles

### 3.1 Least Privilege
Users and systems must be granted the minimum access rights required to perform their specific job function. Access must never be granted by default or convenience. Over-provisioning is treated as a policy violation.

### 3.2 Need-to-Know
Access to sensitive data — including customer PII, financial transaction data, and system credentials — is restricted to those with a documented business requirement. Access justified solely by seniority or convenience is not permitted.

### 3.3 Separation of Duties
Critical business functions must be divided such that no single individual has end-to-end control over a sensitive process. For example, the person who initiates a payment must not be the same person who approves it.

### 3.4 Default Deny
All system access is denied by default. Access is explicitly granted only after an approved access request process has been completed. This applies to both user accounts and system-to-system integrations.

### 3.5 Accountability
Every access action must be attributable to a specific named individual. Shared accounts that prevent individual accountability are prohibited except where technically unavoidable and risk-accepted by the CISO.

## 4. Account Types and Classification

| Account Type | Examples | Requirements |
|---|---|---|
| Standard User Account | Employee email, HR portal, collaboration tools | MFA required. Scoped to role. Password Policy (POL-SEC-001) applies. Reviewed annually. |
| Privileged / Admin Account | Cloud admin console, server root, DB admin | Separate named account (not combined with standard). MFA mandatory (hardware key preferred). Session logging required. Reviewed quarterly. |
| Developer Account | GitHub, CI/CD pipelines, dev/staging systems | No direct production access. MFA required. Pre-commit secret scanning enforced. Reviewed every 6 months. |
| Service Account | API integrations, automated jobs, pipelines | No interactive login. Credentials stored in approved secrets manager. Rotated every 90 days. Named and documented. |
| Vendor / Third-Party | Payment processor access, external auditors | Time-limited. Scoped to minimum required access. MFA required. Access revoked immediately on engagement end. |
| Shared / Generic Account | Legacy systems where individual accounts unavailable | Prohibited where possible. Requires CISO sign-off, full audit logging, and quarterly review of all users with access. |

## 5. Role-Based Access Control (RBAC) Matrix

PayFlow uses a Role-Based Access Control model. Access to systems is assigned to roles, not individuals. Users are assigned the role(s) that correspond to their job function. The matrix below defines permitted access levels for each role across key systems.

**Access Level Legend:** R = Read Only | R/W = Read and Write | A = Full Administrative Access | X = No Access Permitted

| Role / System | Production Systems | Dev / Staging | Payment APIs | Customer PII | Cloud Storage | Admin Console | Source Code Repos | Logs & Monitoring |
|---|---|---|---|---|---|---|---|---|
| Standard Employee | X | X | X | X | X | X | X | X |
| Developer | X | R/W | X | X | R | X | R/W | R |
| Senior Developer / Tech Lead | R | R/W | R | X | R/W | X | R/W | R/W |
| DevOps / Cloud Engineer | R/W | R/W | R | X | R/W | R | R | R/W |
| Security / GRC Analyst | R | R | R | R | R | R | R | R/W |
| IT Administrator | A | A | R | R | A | A | R | A |
| Finance / Operations Staff | X | X | X | R | X | X | X | X |
| Executive (CEO/CTO) | R | R | R | R | R | A | R | R |
| Third-Party / Vendor | X | X | X | X | X | X | X | X |

Access levels in the matrix above represent maximum permitted access. Actual access provisioned to individuals within a role may be further restricted based on the specific business need.

## 6. Access Provisioning and Deprovisioning

### 6.1 Access Provisioning (Granting Access)

All access requests must follow the formalised provisioning process below. Access must never be provisioned informally, verbally, or without documented approval.

| Step | Stage | Owner | Action / Requirement |
|---|---|---|---|
| 1 | Access Request | Employee / Manager | Requestor submits formal access request via IT ticketing system, specifying system, access level, and business justification |
| 2 | Line Manager Approval | Direct Manager | Manager reviews and approves request confirming business need and role relevance within 2 business days |
| 3 | Security Review | CISO / GRC Analyst | For privileged or sensitive access: GRC Analyst reviews against least-privilege principle and risk posture |
| 4 | IT Provisioning | IT Administrator | IT provisions access only to approved systems and role, enforces MFA enrolment, sets appropriate expiry date |
| 5 | Confirmation & Logging | IT / Security | Access grant is logged in the access register with date, approver, system, and access level. User is notified. |

### 6.2 Access Deprovisioning (Revoking Access)

Timely removal of access upon departure or role change is critical. Failure to deprovision access is a common cause of insider risk and orphaned account exploitation.

| Step | Stage | Owner | Action / Requirement |
|---|---|---|---|
| 1 | Trigger Event | HR / Manager | Resignation, termination, role change, or contract end triggers an offboarding notification to IT and Security |
| 2 | Immediate Suspension | IT Administrator | All accounts disabled within 4 hours of departure notification; reduced to 1 hour for involuntary terminations |
| 3 | Credential Revocation | IT / DevOps | All passwords reset, API keys revoked, SSH keys removed, MFA tokens deregistered, VPN access terminated |
| 4 | Access Review | CISO / GRC Analyst | Review confirms complete removal from all systems; shared accounts updated; secrets manager reviewed for service accounts |
| 5 | Documentation | IT / HR | Offboarding checklist signed off and retained for audit purposes. Access register updated to reflect deprovisioning. |

**Audit Requirement:** All access provisioning and deprovisioning actions must be logged in PayFlow's Access Register (maintained by the IT team) and made available for audit review on request.

## 7. Access Reviews

Access rights must be formally reviewed on a scheduled basis to identify and remove excessive, outdated, or inappropriate access. Reviews must be documented and signed off by the relevant manager and the CISO.

| Review Type | Frequency | Scope |
|---|---|---|
| Privileged Access Review | Quarterly | All admin, root, cloud, and developer accounts. Owner: CISO. |
| Standard User Access Review | Semi-Annually | All standard user accounts. Review role alignment. Manager sign-off required. |
| Third-Party Access Review | Quarterly | All external vendor and contractor accounts. Confirm ongoing necessity. Revoke if engagement has ended. |
| Full Access Certification | Annually | Complete review of all accounts across all systems. Includes service accounts, shared accounts, and dormant accounts. |
| Triggered Review | Upon significant event | Role change, promotion, project end, security incident, or organisational restructure. Immediate. |

## 8. Privileged Access Management (PAM)

Privileged accounts pose the highest risk to PayFlow's systems. The following controls govern all privileged access and supplement the general access control requirements above.

| PAM Control | Requirement |
|---|---|
| Privileged Account Inventory | A complete, up-to-date register of all privileged accounts must be maintained and reviewed quarterly by the CISO |
| Just-In-Time (JIT) Access | Where technically feasible, privileged access should be time-limited and granted only for the duration of the specific task |
| Break-Glass / Emergency Accounts | Emergency accounts must be sealed, documented, dual-custody controlled, and every use logged and reviewed within 24 hours |
| Session Recording | All privileged sessions (SSH, RDP, admin console) must be recorded and retained for a minimum of 90 days |
| Shared Account Prohibition | Shared administrative accounts are prohibited. Each administrator must have an individual named account for accountability |
| Separation of Duties | No single individual may have end-to-end control over a critical business process (e.g. both initiate and approve a payment) |
| Privileged Account MFA | Hardware security key (FIDO2) or authenticator app MFA is mandatory for all privileged accounts — no exceptions |

## 9. Remote and Third-Party Access

### 9.1 Remote Access (VPN / SSH)

- All remote access to PayFlow systems must be made exclusively through the approved VPN or SSH gateway
- Direct internet-facing access to internal systems (e.g., RDP exposed to internet) is prohibited
- MFA is mandatory for all remote access connections
- VPN session tokens must expire after 8 hours of inactivity
- Split-tunnelling that bypasses security monitoring is prohibited

### 9.2 Third-Party and Vendor Access

- Third-party access must be formally requested, time-limited, and scoped to the minimum required systems
- Vendor accounts must not have persistent access; access is provisioned on-demand and revoked on task completion
- All third-party access must be logged and subject to the same MFA requirements as PayFlow employees
- Third-party access to production systems or customer data requires written CISO approval
- Security obligations must be documented in vendor contracts and NDAs before access is provisioned

## 10. Production Environment Access Controls

Given the high-value nature of PayFlow's production systems — including live payment processing, customer PII, and financial data — access to production environments is subject to additional restrictions.

**Risk Remediation Notice:** CRITICAL: No developer should have unrestricted, persistent access to the production environment. This control directly remediates Risk R-003 (Score: 20 — CRITICAL) from the PayFlow Risk Register.

- Production access requires explicit approval from the CTO and CISO on a per-task basis
- All production access must be time-limited with automatic revocation after task completion
- All production changes must follow a formal change management process with rollback capability
- Production, staging, and development environments must be strictly separated with no shared credentials
- No code may be deployed directly to production without passing automated security testing in a staging environment
- All production access sessions must be logged and auditable for a minimum of 180 days

## 11. Access Monitoring and Anomaly Detection

Access control is only effective if access activity is monitored. The following logging and alerting requirements apply across all PayFlow systems.

| Event Type | Monitoring Requirement |
|---|---|
| Failed login attempts | Alert after 3 consecutive failures on privileged accounts; 5 on standard accounts. Lockout enforced. |
| After-hours access | Flag and alert on access to sensitive systems outside of business hours (8am–8pm WAT) for investigation. |
| Privileged account activity | All privileged session activity logged in full. Alerts on new privilege grants, bulk data access, or configuration changes. |
| Data exfiltration indicators | Alert on bulk downloads, unusual API call volumes, or access to PII by non-standard roles. |
| Account creation / deletion | All account lifecycle events logged and alerting sent to CISO and IT team. |
| Access from new geolocation | Flag and alert on first-time access from an unrecognised country or IP range. |

## 12. Policy Violations

Violations of this policy will be escalated through HR and the CISO and may result in disciplinary action up to and including termination of employment and legal proceedings.

| Violation | Severity | Consequence |
|---|---|---|
| Accessing systems beyond assigned role | HIGH | Immediate access suspension; formal investigation; disciplinary action |
| Sharing access credentials with another user | HIGH | Formal warning; access review; mandatory re-training; potential dismissal |
| Bypassing access control mechanisms | CRITICAL | Immediate account suspension; security incident declared; potential legal action |
| Failure to report a suspected breach | HIGH | Formal written warning; mandatory security training; performance review |
| Granting access without proper approval | HIGH | Revocation of provisioning rights; review of all grants made; formal warning |
| Retaining access after role change / exit | MEDIUM | Immediate access removal; IT audit of provisioning process; documented finding |
| Using another person's account | CRITICAL | Immediate suspension of both accounts; investigation; potential termination |

## 13. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| All Users | Comply with access restrictions; report unusual access events; never share credentials or attempt to exceed assigned access |
| Line Managers | Approve access requests for their team; notify IT of role changes or departures within 24 hours |
| IT Administrator | Implement and enforce access controls; maintain the access register; execute provisioning and deprovisioning in defined timeframes |
| DevOps / Engineering | Enforce environment separation; maintain RBAC configurations; ensure no hardcoded credentials; implement secrets management |
| CISO / GRC Analyst | Own this policy; approve privileged access exceptions; conduct access reviews; manage access-related incidents |
| HR Department | Trigger onboarding and offboarding notifications; ensure policy acknowledgement at onboarding |
| CEO / CTO | Approve this policy; approve production access for privileged users; ensure resources for implementation |
