# PASSWORD POLICY
**PayFlow Fintech Nigeria Ltd.**

## 1. Purpose

This Password Policy establishes the minimum standards for the creation, protection, management, and expiry of passwords used to access PayFlow's information systems, applications, cloud infrastructure, and data. It exists to reduce the risk of unauthorised access resulting from weak, stolen, or compromised credentials — a risk identified as HIGH to CRITICAL in PayFlow's Week 2 Risk Assessment (risks R-003 and R-004).

This policy applies to all PayFlow employees, contractors, interns, and any third party granted access to PayFlow systems, and covers all user accounts including standard user, administrative, service, and shared accounts.

## 2. Scope

This policy applies to:

- All employees, contractors, and temporary staff with access to PayFlow systems
- All information systems, applications, APIs, cloud platforms, databases, and network devices
- All account types: standard user accounts, privileged/administrative accounts, service accounts, and shared accounts
- All access methods: web applications, VPN, SSH, remote desktop, and mobile device access

## 3. Password Requirements

All passwords must meet the minimum requirements defined in the table below. Where a system cannot technically enforce these requirements, the limitation must be documented and an approved compensating control implemented.

| Requirement | Standard | Privileged / Admin Accounts |
|---|---|---|
| Minimum Length | 12 characters | 16 characters minimum |
| Character Complexity | Must include: uppercase, lowercase, number, and at least one special character (e.g. ! @ # $ % ^) | Same requirements apply — passphrase format encouraged |
| Maximum Password Age | 90 days | 60 days |
| Minimum Password Age | 1 day (prevents immediate re-use) | 1 day |
| Password History | Cannot reuse last 10 passwords | Cannot reuse last 12 passwords |
| Account Lockout Threshold | 5 failed attempts | 3 failed attempts |
| Lockout Duration | 15 minutes (auto-unlock) | 30 minutes; manual unlock by IT Admin |
| Multi-Factor Authentication (MFA) | Required for all accounts | Mandatory; hardware token or authenticator app preferred |
| Password Manager | Strongly recommended | Mandatory — corporate-approved password manager required |
| Default/Temporary Passwords | Must be changed on first login | Must be changed on first login; cannot be reused |

## 4. Prohibited Passwords

The following password types are strictly prohibited across all PayFlow systems. IT systems must, where technically feasible, be configured to reject such passwords at the point of creation or change.

| Category | Examples / Description |
|---|---|
| Personal Information | Name, date of birth, phone number, email address, or any combination thereof |
| Dictionary Words | Single common words (e.g. 'password', 'welcome', 'secure') — even with number substitutions like '0' for 'o' |
| Keyboard Patterns | Sequences such as 'qwerty', '123456', 'abcdef', 'asdfgh' |
| Company Name / Variants | 'payflow', 'payflow1', 'PayFlow!', or any easily guessable variation |
| Repeated Characters | 'aaaa1111', '1111aaaa' — passwords with four or more consecutive identical characters |
| Previously Breached | Any password identified in publicly known data breaches (checked against HaveIBeenPwned API or equivalent) |
| Blank / Empty | Systems must not allow blank passwords under any circumstance |

## 5. Multi-Factor Authentication (MFA) Requirements

Passwords alone are insufficient for securing access to PayFlow's financial systems. Multi-Factor Authentication (MFA) is mandatory and must be enforced across all systems where technically feasible.

### 5.1 Mandatory MFA Systems

- All cloud platform accounts (AWS, GCP, Azure, or equivalent)
- All email and collaboration accounts (Google Workspace, Microsoft 365)
- All administrative and privileged system accounts
- All VPN and remote access connections
- All payment processing system access
- All developer access to production environments

### 5.2 Approved MFA Methods

- Authenticator app (Google Authenticator, Microsoft Authenticator, Authy) — Preferred
- Hardware security key (FIDO2 / YubiKey) — Required for privileged accounts
- Time-based One-Time Password (TOTP)
- SMS OTP — Permitted as fallback only; discouraged due to SIM-swap risk

### 5.3 MFA Exceptions

MFA exceptions may only be granted by the CISO or designated GRC Analyst and must be:

- Documented in writing with a stated business justification
- Time-limited (maximum 30 days) with a scheduled review date
- Compensated with an alternative approved control

## 6. Password Storage and Handling

### 6.1 System-Side Storage

- All system-stored passwords must be hashed using bcrypt, Argon2, or PBKDF2 with a minimum work factor appropriate to current computing capability
- Passwords must never be stored in plaintext, reversibly encrypted form, or in application logs
- Legacy systems using MD5 or SHA-1 for password hashing must be flagged as non-compliant and remediated within 60 days

### 6.2 User-Side Handling

- Employees must not write passwords on physical paper, sticky notes, or whiteboards
- Employees must not store passwords in unencrypted documents, spreadsheets, or email
- Approved corporate password managers must be used for storing and generating passwords
- Passwords must never be transmitted via email, SMS, or instant messaging — even internally
- Passwords must never be shared between users under any circumstances

### 6.3 Service and API Accounts

- Service account passwords and API keys must be stored exclusively in approved secrets management tools (e.g. AWS Secrets Manager, HashiCorp Vault)
- Hardcoded credentials in source code are strictly prohibited (see Risk R-001)
- API keys must be rotated every 90 days or immediately upon suspected compromise

## 7. Password Reset and Recovery Procedures

### 7.1 Self-Service Reset

Where a self-service password reset facility is available, it must require identity verification via MFA before allowing a reset. Security questions alone are not a sufficient verification method.

### 7.2 IT-Assisted Reset

- IT-assisted resets must only be performed after verifying the requestor's identity through an approved channel (not email or phone alone)
- All IT-assisted resets must be logged with timestamp, requestor, and approver details
- A temporary password issued by IT must require immediate change on first login

### 7.3 Emergency Access

Emergency or break-glass account access must be governed by a separate Privileged Access Management procedure and must be logged, time-limited, and reviewed by the CISO within 24 hours of use.

## 8. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| All Staff / Users | Comply with this policy; protect own credentials; report suspected compromise immediately |
| IT / DevOps Team | Enforce technical controls; configure account lockout and MFA; maintain secrets management tooling |
| HR Department | Ensure policy acceptance at onboarding; trigger account disabling upon employee departure |
| CISO / GRC Analyst | Own, maintain, and review this policy; investigate policy violations; approve exceptions |
| Engineering Leads | Ensure no hardcoded credentials in code; enforce pre-commit secret scanning in repositories |
| CEO / CTO | Approve this policy and any material changes; ensure adequate resources for implementation |

## 9. Policy Violations

Violations of this policy will be treated seriously and may result in disciplinary action up to and including termination of employment, and where applicable, legal proceedings.

| Violation Type | Severity | Consequence |
|---|---|---|
| Sharing password with another user | HIGH | Formal warning; potential disciplinary action; access review |
| Failure to change temporary password | MEDIUM | Account suspension until resolved; reminder notification |
| Writing down password in accessible place | MEDIUM | Verbal/written warning; mandatory security awareness training |
| Using a prohibited/weak password | MEDIUM | Forced password reset; documented in personnel file |
| Deliberate bypass of MFA requirement | HIGH | Immediate access suspension; investigation; potential dismissal |
| Sharing credentials with a third party | CRITICAL | Immediate suspension; formal investigation; potential legal action |

All violations must be reported to the CISO or GRC Analyst within 24 hours of discovery. Suspected credential compromise must be treated as a security incident and escalated through the Incident Response Plan.
