# ISO/IEC 27001:2022 COMPLIANCE CHECKLIST
**PayFlow Fintech Nigeria Ltd. — GRC Programme Week 4 Deliverable**

## 1. Purpose and Scope

This compliance checklist maps PayFlow's current information security posture against the requirements of ISO/IEC 27001:2022 — the international standard for Information Security Management Systems (ISMS). It covers all mandatory clauses (4–10) and all 93 controls across the four Annex A control themes.

The assessment is based on the findings of the Week 1 Risk Register, Week 2 Risk Assessment, and the Week 3 security policies. It identifies gaps between PayFlow's current state and the requirements for ISO 27001 certification, assigns a compliance status to each control, and prioritizes remediation activity.

**Assessment Overview:** Framework: ISO/IEC 27001:2022 | Total Controls Assessed: 118 | Compliant: 0 | Partial: 35 | Non-Compliant: 80 | N/A: 3

## 2. Status Key and Scoring Methodology

| Status | Meaning | Description |
|---|---|---|
| COMPLIANT | Fully Met | Control fully implemented, documented, and evidenced. Meets ISO 27001 requirement. |
| PARTIAL | Partially Met | Control partially implemented. Policy or process exists but is incomplete, unenforced, or not consistently applied. |
| NON-COMPLIANT | Not Met | Control not in place. No evidence of implementation. Requires immediate attention. |
| IN PROGRESS | Active Remediation | Control is actively being implemented as part of the current GRC programme. |
| N/A | Not Applicable | Control is not applicable to PayFlow's current operating model or scope. |

## 3. Executive Compliance Summary

The table below presents the overall compliance position across all 118 ISO/IEC 27001:2022 controls assessed for PayFlow.

| Status | Count | % of Total |
|---|---|---|
| COMPLIANT | 0 | 0% |
| PARTIAL | 35 | 30% |
| NON-COMPLIANT | 80 | 68% |
| N/A | 3 | 3% |

PayFlow is at a very early stage of ISMS implementation. The majority of non-compliance findings are driven by the absence of foundational governance structures, documented policies, and technical controls — all of which are being addressed through this GRC programme. The partial-compliance findings represent areas where initial work (Password Policy, Access Control Policy, Risk Register) has begun but is not yet fully implemented or evidenced.

### 3.1 Remediation Priority Summary

| Priority | Controls | Required Action |
|---|---|---|
| CRITICAL | 29 | Immediate action — before any partnership/audit |
| HIGH | 60 | Remediate within 30 days |
| MEDIUM | 21 | Remediate within 90 days |
| LOW | 5 | Monitor and review annually |

## 4. Full ISO/IEC 27001:2022 Compliance Checklist

The checklist below covers all applicable clauses and controls. Each row documents the control ID, what the standard requires, PayFlow's current compliance status, the evidence or rationale for that status, and identified gaps.

### Clause 4 — Context of the Organization

| Ctrl | Control / Requirement | What ISO 27001 Requires | Status | Evidence / Current State at PayFlow | Gap / Finding |
|---|---|---|---|---|---|
| 4.1 | Understanding the Organization | Identify internal and external issues relevant to the ISMS purpose and strategic direction | NON-COMPLIANT | No formal context analysis has been conducted. Business strategy not linked to security governance. | No ISMS scope or organizational context document exists. |
| 4.2 | Understanding Interested Parties | Identify stakeholders and their requirements relevant to the ISMS | NON-COMPLIANT | Investors have raised concerns post-API incident. No stakeholder register exists. | Stakeholder requirements (regulatory, investor, partner) not documented or tracked. |
| 4.3 | Determining the Scope of the ISMS | Define and document the scope of the ISMS | NON-COMPLIANT | No ISMS scope statement exists. Cloud systems, APIs, and PII are in scope but not defined. | ISMS scope document must be created before certification can begin. |
| 4.4 | ISMS Establishment | Establish, implement, maintain and continually improve an ISMS | NON-COMPLIANT | No ISMS programme exists. GRC engagement is the first formal step. | Full ISMS must be designed and implemented. This checklist initiates that process. |

### Clause 5 — Leadership

| Ctrl | Control / Requirement | What ISO 27001 Requires | Status | Evidence / Current State at PayFlow | Gap / Finding |
|---|---|---|---|---|---|
| 5.1 | Leadership and Commitment | Top management must demonstrate commitment to the ISMS | PARTIAL | CEO has acknowledged security governance need; GRC analyst engaged. No formal ISMS policy signed. | Executive ISMS policy statement not yet approved or published. |
| 5.2 | Information Security Policy | Establish and communicate an information security policy | NON-COMPLIANT | No overarching information security policy exists. Password and Access Control Policies drafted (Wk 3). | Top-level information security policy must be created, approved, and communicated to all staff. |
| 5.3 | Organizational Roles and Responsibilities | Assign and communicate ISMS roles and responsibilities | PARTIAL | GRC Analyst assigned. No CISO formally appointed. IT roles informally defined. | Formal RACI for ISMS roles must be documented, approved, and communicated. |

### Clause 6 — Planning

| Ctrl | Control / Requirement | What ISO 27001 Requires | Status | Evidence / Current State at PayFlow | Gap / Finding |
|---|---|---|---|---|---|
| 6.1.1 | Actions to Address Risks and Opportunities — General | Determine risks/opportunities affecting the ISMS | PARTIAL | Risk Register (Wk 1) and Risk Matrix (Wk 2) completed. No formal treatment plan yet. | Risk treatment plan not yet produced. Wk 6 deliverable will address this. |
| 6.1.2 | Information Security Risk Assessment | Perform risk assessments using defined criteria | PARTIAL | Qualitative 5x5 risk assessment completed (Wk 2). No defined risk acceptance criteria documented. | Risk acceptance criteria and formal risk assessment methodology must be documented. |
| 6.1.3 | Information Security Risk Treatment | Select and implement risk treatment options | NON-COMPLIANT | No risk treatment plan exists. Controls partially implemented (Password/Access policies). | Risk treatment plan must map controls to all identified risks. Required for Annex A compliance. |
| 6.2 | Information Security Objectives | Establish measurable information security objectives | NON-COMPLIANT | No formal security objectives or KPIs defined for PayFlow. | Security objectives (e.g. 0 critical incidents, 100% MFA adoption) must be set and tracked. |
| 6.3 | Planning of Changes | Plan changes to the ISMS in a controlled manner | NON-COMPLIANT | No change management process exists. Developers push updates without review. | Change management policy and formal change control process must be implemented. |

### Clause 7 — Support

| Ctrl | Control / Requirement | What ISO 27001 Requires | Status | Evidence / Current State at PayFlow | Gap / Finding |
|---|---|---|---|---|---|
| 7.1 | Resources | Provide resources needed for ISMS establishment and operation | PARTIAL | GRC analyst engaged. No dedicated security budget or tooling formally allocated. | Security budget, tooling (SIEM, PAM, CSPM), and staffing plan must be formally approved. |
| 7.2 | Competence | Ensure ISMS personnel have the necessary competence | PARTIAL | GRC analyst has relevant knowledge. No formal training records or competency assessments for IT staff. | Training records, role-based competency requirements, and certifications must be tracked. |
| 7.3 | Awareness | Ensure staff awareness of the information security policy | NON-COMPLIANT | No security awareness programme exists. Staff onboarded without security briefings. | Mandatory security awareness training must be implemented and tracked for all staff. |
| 7.4 | Communication | Define internal/external communication requirements | NON-COMPLIANT | No formal communication plan for security matters (incidents, policy changes, audit findings). | ISMS communication plan must be created covering internal and external audiences. |
| 7.5 | Documented Information | Create, control, and maintain required ISMS documentation | PARTIAL | Risk Register, Risk Matrix, Password Policy, Access Control Policy exist. Many required docs missing. | Full ISMS documentation set must be developed (policy, procedures, records, evidence). |

### Clause 8 — Operation

| Ctrl | Control / Requirement | What ISO 27001 Requires | Status | Evidence / Current State at PayFlow | Gap / Finding |
|---|---|---|---|---|---|
| 8.1 | Operational Planning and Control | Plan, implement, and control ISMS processes | NON-COMPLIANT | No operational ISMS processes defined. No separation of dev/staging/prod environments. | Operational security procedures must be documented and enforced across all teams. |
| 8.2 | Information Security Risk Assessment | Perform risk assessments at planned intervals | PARTIAL | Initial risk assessment completed (Wk 2). No schedule for repeat assessments defined. | Annual and event-triggered risk assessment schedule must be established and documented. |
| 8.3 | Information Security Risk Treatment | Implement the risk treatment plan | NON-COMPLIANT | Risk treatment plan not yet developed. Controls partially in place. | Risk treatment plan (Wk 6 deliverable) must be formally approved and tracked. |

### Clause 9 — Performance Evaluation

| Ctrl | Control / Requirement | What ISO 27001 Requires | Status | Evidence / Current State at PayFlow | Gap / Finding |
|---|---|---|---|---|---|
| 9.1 | Monitoring, Measurement, Analysis and Evaluation | Define and measure ISMS performance metrics | NON-COMPLIANT | No security monitoring or KPI tracking in place. No SIEM or logging strategy. | Security metrics framework must be defined. Logging/SIEM must be deployed. |
| 9.2 | Internal Audit | Conduct internal audits of the ISMS | NON-COMPLIANT | No internal audits ever conducted. This GRC programme is the first structured assessment. | Internal audit programme must be established with defined scope, schedule, and methodology. |
| 9.3 | Management Review | Top management must review the ISMS periodically | NON-COMPLIANT | No management review process exists. Security has not been a board-level agenda item. | Quarterly management review meetings for ISMS performance must be scheduled and minuted. |

### Clause 10 — Continual Improvement

| Ctrl | Control / Requirement | What ISO 27001 Requires | Status | Evidence / Current State at PayFlow | Gap / Finding |
|---|---|---|---|---|---|
| 10.1 | Continual Improvement | Continually improve ISMS suitability and effectiveness | NON-COMPLIANT | No improvement processes in place. No lessons-learned reviews conducted. | A formal continual improvement process (Plan-Do-Check-Act) must be embedded into operations. |
| 10.2 | Nonconformity and Corrective Action | Address nonconformities and implement corrective actions | NON-COMPLIANT | API key incident had no formal corrective action or root cause analysis documented. | A nonconformity and corrective action procedure must be created and applied to all findings. |

### Annex A.5 — Organizational Controls

| Ctrl | Control / Requirement | What ISO 27001 Requires | Status | Evidence / Current State at PayFlow | Gap / Finding |
|---|---|---|---|---|---|
| A.5.1 | Policies for Information Security | Information security policies approved by management and communicated | NON-COMPLIANT | No overarching information security policy. Password and access policies drafted but not approved. | Top-level information security policy required. Existing draft policies need formal sign-off. |
| A.5.2 | Information Security Roles and Responsibilities | Define and allocate security roles | PARTIAL | GRC analyst in place; roles informally distributed. No formal ISMS RACI. | Formal RACI must be published and accepted by all role holders. |
| A.5.3 | Segregation of Duties | Separate conflicting duties to reduce risk | NON-COMPLIANT | Developers have full production access. No separation between build, deploy, and approve. | Segregation of duties matrix must be implemented. Remediates R-003. |
| A.5.4 | Management Responsibilities | Managers must promote security to their teams | PARTIAL | Leadership has endorsed the GRC programme. No formal management security mandate communicated. | Management security responsibilities must be documented in JDs and formally communicated. |
| A.5.5 | Contact with Authorities | Maintain contacts with relevant authorities (regulators, law enforcement) | NON-COMPLIANT | No documented contacts with CBN, NDPC, NCC or law enforcement for incident escalation. | Contact register with regulatory bodies must be established and maintained. |
| A.5.6 | Contact with Special Interest Groups | Engage with security forums and threat intelligence sources | NON-COMPLIANT | No engagement with threat intelligence or fintech security communities. | Subscribe to threat intelligence feeds (e.g., FS-ISAC, CERT-NG) relevant to fintech. |
| A.5.7 | Threat Intelligence | Collect and analyze relevant threat intelligence | NON-COMPLIANT | No threat intelligence programme exists. No awareness of current attack patterns targeting fintech. | Implement threat intelligence feed and integrate into risk reviews. |
| A.5.8 | Information Security in Project Management | Include security in project management | NON-COMPLIANT | No security requirements in the SDLC or project onboarding process. | Security must be embedded into project initiation and sprint planning (Secure SDLC). |
| A.5.9 | Inventory of Information and Other Assets | Maintain an asset inventory | NON-COMPLIANT | No formal asset inventory. Week 1 GRC register is the first asset documentation. | Formal, maintained asset register must be created and reviewed quarterly. |
| A.5.10 | Acceptable Use of Information and Assets | Define and enforce acceptable use rules | NON-COMPLIANT | No Acceptable Use Policy exists. | AUP must be created, communicated to all staff, and signed at onboarding. |
| A.5.11 | Return of Assets | Ensure assets are returned on employment termination | PARTIAL | No formal offboarding asset return process. Access deprovisioning procedure drafted (POL-SEC-002). | Asset return checklist must be added to the offboarding procedure. |
| A.5.12 | Classification of Information | Classify information according to sensitivity | NON-COMPLIANT | No data classification scheme exists. PII, financial data, and logs treated without differentiation. | Data classification policy (Public / Internal / Confidential / Restricted) must be created. |
| A.5.13 | Labelling of Information | Apply labels in accordance with classification scheme | NON-COMPLIANT | No labelling of documents, data, or systems. | Labelling standards must be defined and applied once classification policy is in place. |
| A.5.14 | Information Transfer | Define rules for transferring information internally and externally | NON-COMPLIANT | No data transfer controls or policies. Sensitive data sharing via email not restricted. | Data transfer policy including encryption-in-transit requirements must be implemented. |
| A.5.15 | Access Control | Implement access control policy | PARTIAL | Access Control Policy (POL-SEC-002) drafted. RBAC not yet technically enforced. | Access control policy must be fully implemented and technically enforced. |
| A.5.16 | Identity Management | Manage the full lifecycle of identities | PARTIAL | Accounts created during onboarding. No formal identity lifecycle management process. | Identity management process covering creation, modification, and deletion must be formalized. |
| A.5.17 | Authentication Information | Manage authentication credentials securely | PARTIAL | Password policy drafted (POL-SEC-001). MFA not consistently enforced. API keys exposed previously. | Password policy must be technically enforced. MFA mandatory. Secrets manager required. |
| A.5.18 | Access Rights | Grant, review, and revoke access rights | PARTIAL | Access review process defined in POL-SEC-002. Not yet operationally active. | Quarterly access reviews must begin immediately. Access register must be established. |
| A.5.19 | Information Security in Supplier Relationships | Address security in supplier agreements | NON-COMPLIANT | Third-party payment processors integrated without security vetting or contractual security terms. | Supplier security policy and contract clauses must be established for all critical vendors. |
| A.5.20 | Addressing Security in Supplier Agreements | Include security requirements in supplier contracts | NON-COMPLIANT | No security SLAs, right-to-audit clauses, or data protection terms in vendor contracts. | All critical supplier contracts must be reviewed and updated with security requirements. |
| A.5.21 | Managing Security in the ICT Supply Chain | Address security risks in the ICT supply chain | NON-COMPLIANT | No assessment of third-party software libraries, cloud providers, or payment API dependencies. | Supply chain risk assessment must be conducted for all critical technology dependencies. |
| A.5.22 | Monitoring, Review and Change Management of Supplier Services | Monitor and review supplier performance | NON-COMPLIANT | No supplier performance monitoring or security review process. | Annual supplier security reviews must be scheduled and documented. |
| A.5.23 | Information Security for Use of Cloud Services | Manage security for cloud service use | NON-COMPLIANT | Cloud services used without defined security baseline, encryption policy, or access controls. | Cloud security policy, CSPM tooling, and encryption baseline must be implemented. |
| A.5.24 | Information Security Incident Management Planning | Plan for incident management | NON-COMPLIANT | No Incident Response Plan exists. Previous API key incident handled informally. | IRP must be developed, tested, and communicated. Directly remediates R-007. |
| A.5.25 | Assessment and Decision on Information Security Events | Assess and classify security events | NON-COMPLIANT | No event triage or classification process. No SIEM in place. | Security event classification criteria and triage process must be defined. |
| A.5.26 | Response to Information Security Incidents | Respond to security incidents according to plan | NON-COMPLIANT | No formal response process. No assigned IR team or communication protocol. | IR response procedures, roles, and escalation paths must be documented and drilled. |
| A.5.27 | Learning from Information Security Incidents | Use incidents to improve the ISMS | NON-COMPLIANT | No post-incident review process. API key incident produced no documented lessons learned. | Post-incident review (PIR) process must be formalised and applied to all incidents. |
| A.5.28 | Collection of Evidence | Collect and preserve evidence for incidents | NON-COMPLIANT | No digital forensics capability or evidence preservation procedure. | Evidence collection procedures and log retention requirements must be documented. |
| A.5.29 | Information Security During Disruption | Maintain security during business disruptions | NON-COMPLIANT | No Business Continuity Plan. Backups exist but are untested. | BCP must be developed and tested. Backup restoration must be verified quarterly. |
| A.5.30 | ICT Readiness for Business Continuity | Plan ICT continuity for business disruption scenarios | NON-COMPLIANT | No ICT continuity plan or RTO/RPO targets defined. | RTO/RPO must be defined for all critical systems and documented in BCP. |
| A.5.31 | Legal, Statutory, Regulatory and Contractual Requirements | Identify and comply with applicable legal requirements | NON-COMPLIANT | No register of applicable regulations (NDPA, CBN, PCI DSS, GDPR for EU customers). | Legal and regulatory register must be compiled and reviewed annually. |
| A.5.32 | Intellectual Property Rights | Protect intellectual property rights | PARTIAL | Software licensed through GitHub. No formal IP rights register or review. | IP rights register and software licence management process must be implemented. |
| A.5.33 | Protection of Records | Protect records from loss, falsification, and unauthorized access | NON-COMPLIANT | No records management policy. Logs and backups stored without encryption or access controls. | Records retention and protection policy must be created and technically enforced. |
| A.5.34 | Privacy and Protection of PII | Protect PII in accordance with applicable law | NON-COMPLIANT | PII stored without consistent encryption. No privacy policy or DPIA conducted. | NDPA/GDPR compliance review must be conducted. Data Protection Officer role must be defined. |
| A.5.35 | Independent Review of Information Security | Conduct periodic independent reviews of ISMS | NON-COMPLIANT | No independent review or external audit ever conducted. | Annual independent ISMS review must be scheduled. External auditor should be engaged. |
| A.5.36 | Compliance with Security Policies | Verify compliance with policies and procedures | NON-COMPLIANT | No compliance monitoring or policy violation tracking. | Compliance monitoring process and audit schedule must be established. |
| A.5.37 | Documented Operating Procedures | Document and maintain operating procedures | NON-COMPLIANT | No documented operating procedures for IT, DevOps, or security operations. | SOPs for all critical operations must be created, approved, and version-controlled. |

### Annex A.6 — People Controls

| Ctrl | Control / Requirement | What ISO 27001 Requires | Status | Evidence / Current State at PayFlow | Gap / Finding |
|---|---|---|---|---|---|
| A.6.1 | Screening | Screen candidates before employment according to role sensitivity | NON-COMPLIANT | No background screening process for employees with access to financial or PII data. | Background check process must be implemented for all roles with system access. |
| A.6.2 | Terms and Conditions of Employment | Security responsibilities in employment contracts | PARTIAL | Employment contracts exist. No specific information security obligations documented. | Security responsibilities and consequences of breach must be added to employment contracts. |
| A.6.3 | Information Security Awareness, Education and Training | Provide security awareness training | NON-COMPLIANT | No security awareness training programme exists. Onboarding skips security briefings. | Mandatory security awareness training at onboarding and annually thereafter must be implemented. |
| A.6.4 | Disciplinary Process | Apply a disciplinary process for security violations | PARTIAL | HR disciplinary process exists generally. No specific information security violation procedures. | Security-specific disciplinary procedure must be documented and referenced in policies. |
| A.6.5 | Responsibilities After Termination or Change | Maintain security obligations post-employment | PARTIAL | Access deprovisioning defined in POL-SEC-002. No NDA or confidentiality obligations post-departure. | Post-employment confidentiality obligations must be in employment contracts. Access removed per policy. |
| A.6.6 | Confidentiality or Non-Disclosure Agreements | Require NDAs for access to sensitive information | PARTIAL | NDAs not consistently used with contractors or third parties. | NDAs must be required for all staff, contractors, and vendors before access is granted. |
| A.6.7 | Remote Working | Protect information accessed/processed during remote working | NON-COMPLIANT | No remote working security policy. No VPN enforcement documented. | Remote working security policy must be created covering VPN, device management, and home network requirements. |
| A.6.8 | Information Security Event Reporting | Report security events and weaknesses | NON-COMPLIANT | No security event reporting channel or process. API key incident discovered externally. | Security event reporting mechanism (email alias, ticketing) must be established and communicated. |

### Annex A.7 — Physical Controls

| Ctrl | Control / Requirement | What ISO 27001 Requires | Status | Evidence / Current State at PayFlow | Gap / Finding |
|---|---|---|---|---|---|
| A.7.1 | Physical Security Perimeters | Define and protect physical security perimeters | PARTIAL | Office premises exist with basic physical access. No documented security perimeter controls. | Physical access policy for office and server areas must be documented and enforced. |
| A.7.2 | Physical Entry | Control physical access to secure areas | PARTIAL | Offices have door locks. No access logs, swipe cards, or CCTV documented. | Physical access controls and logging for server rooms and sensitive areas must be implemented. |
| A.7.3 | Securing Offices, Rooms and Facilities | Apply physical security to offices and work areas | PARTIAL | Standard office security in place. No clean-desk policy or visitor management. | Clean-desk policy and visitor management procedure must be implemented. |
| A.7.4 | Physical Security Monitoring | Monitor physical premises for unauthorized access | NON-COMPLIANT | No CCTV or physical intrusion detection documented. | Physical monitoring (CCTV, alarm systems) should be implemented or documented. |
| A.7.5 | Protecting Against Physical and Environmental Threats | Protect against environmental threats (fire, flood, power) | PARTIAL | Cloud-hosted systems have provider-managed physical resilience. Office UPS status unknown. | Cloud provider physical controls must be reviewed. Office environment risk assessment required. |
| A.7.6 | Working in Secure Areas | Apply controls for working in secure areas | N/A | PayFlow is primarily cloud-based. No dedicated data centre on-premises. | N/A — Cloud provider responsible for secure area controls. Vendor review should confirm. |
| A.7.7 | Clear Desk and Clear Screen | Implement clear desk and clear screen policies | NON-COMPLIANT | No clear desk or screen lock policy. Sensitive data may be visible in office environment. | Clear desk/screen policy must be drafted and enforced. Inactivity screen locks must be configured. |
| A.7.8 | Equipment Siting and Protection | Protect equipment from physical threats | PARTIAL | Employee devices issued but not tracked in an asset register. No device encryption confirmed. | Device encryption (BitLocker/FileVault) must be enforced. Asset register must include all endpoints. |
| A.7.9 | Security of Assets Off-Premises | Protect off-premises assets | NON-COMPLIANT | No policy for handling of company devices or data off-premises or when working remotely. | Remote working and portable device policy must be created. |
| A.7.10 | Storage Media | Manage storage media through lifecycle | PARTIAL | Cloud storage is primary. Some local USB/portable media use may occur. | Media handling policy covering encryption, labelling, and secure disposal must be documented. |
| A.7.11 | Supporting Utilities | Protect supporting utilities (power, cooling, network) | PARTIAL | Cloud-hosted systems benefit from provider utility controls. Office utilities not assessed. | Office utility resilience (UPS, backup connectivity) should be assessed and documented. |
| A.7.12 | Cabling Security | Protect power and data cabling | N/A | PayFlow is cloud-first. Physical cabling risks are managed by cloud provider. | N/A — Review cloud provider SAS 70 / SOC 2 report to verify cabling security controls. |
| A.7.13 | Equipment Maintenance | Maintain equipment to ensure availability and integrity | PARTIAL | Employee devices maintained informally. No scheduled maintenance or patch management policy. | Patch management and device maintenance schedule must be implemented. |
| A.7.14 | Secure Disposal or Re-use of Equipment | Dispose of equipment securely | NON-COMPLIANT | No documented device disposal or data wiping procedure. | Secure device disposal procedure (NIST 800-88 or equivalent) must be documented. |

### Annex A.8 — Technological Controls

| Ctrl | Control / Requirement | What ISO 27001 Requires | Status | Evidence / Current State at PayFlow | Gap / Finding |
|---|---|---|---|---|---|
| A.8.1 | User Endpoint Devices | Protect information on user endpoint devices | NON-COMPLIANT | No endpoint management policy (MDM). Device encryption status unknown. | MDM solution must be deployed. Device encryption and screen lock must be enforced. |
| A.8.2 | Privileged Access Rights | Restrict and manage privileged access rights | NON-COMPLIANT | Developers have broad admin access. No PAM tool in place. | PAM controls per POL-SEC-002 must be technically implemented. Admin accounts must be inventoried. |
| A.8.3 | Information Access Restriction | Restrict access to information and functions | PARTIAL | Access Control Policy drafted. RBAC not yet technically enforced on all systems. | RBAC must be fully configured and tested across all production systems. |
| A.8.4 | Access to Source Code | Restrict access to source code | NON-COMPLIANT | Developers have unrestricted access to all repositories. No branch protection or code review enforcement. | Branch protection rules, mandatory code review, and repository access controls must be configured. |
| A.8.5 | Secure Authentication | Implement secure authentication mechanisms | PARTIAL | MFA required per Password Policy. Not yet uniformly enforced across all systems. | SSO with MFA enforcement must be deployed. All accounts must be enrolled. |
| A.8.6 | Capacity Management | Monitor and manage resource usage | NON-COMPLIANT | No capacity monitoring in place. No alerting on resource thresholds. | Cloud resource monitoring and alerting must be configured (e.g., AWS CloudWatch). |
| A.8.7 | Protection Against Malware | Implement malware protection controls | NON-COMPLIANT | No documented endpoint protection or malware prevention tooling. | Endpoint protection (EDR/antivirus) must be deployed to all company devices. |
| A.8.8 | Management of Technical Vulnerabilities | Identify and manage technical vulnerabilities | NON-COMPLIANT | No vulnerability scanning, patch management, or penetration testing programme. | Vulnerability management programme including monthly scanning and quarterly pentesting required. |
| A.8.9 | Configuration Management | Define and manage security configurations | NON-COMPLIANT | No documented security baseline configurations for cloud, servers, or endpoints. | Hardened configuration baselines (CIS Benchmarks) must be defined and applied. |
| A.8.10 | Information Deletion | Delete information when no longer required | NON-COMPLIANT | No data retention or deletion policy. Old data may be indefinitely retained. | Data retention schedule and secure deletion procedure must be created. |
| A.8.11 | Data Masking | Mask PII and sensitive data where appropriate | NON-COMPLIANT | No data masking applied in non-production environments. Developers may have access to real PII. | Data masking must be applied to all non-production environments containing PII. |
| A.8.12 | Data Leakage Prevention | Prevent unauthorised data disclosure | NON-COMPLIANT | No DLP tools or controls. API key was leaked to public GitHub (R-001). | DLP controls must be implemented. Pre-commit scanning and data egress monitoring required. |
| A.8.13 | Information Backup | Back up information and test recovery | PARTIAL | Backups exist but are untested. No documented backup schedule or recovery test results. | Backup schedule must be formalized. Quarterly restoration tests must be conducted and documented. |
| A.8.14 | Redundancy of Information Processing Facilities | Implement redundancy for critical systems | PARTIAL | Cloud provider offers availability zones. PayFlow has not configured multi-AZ or failover. | Multi-AZ deployment and failover configuration must be implemented for all critical services. |
| A.8.15 | Logging | Implement logging for security events | NON-COMPLIANT | Minimal logging in place. Logs and backups in cloud buckets without access controls. | Centralized logging (SIEM) must be deployed. Log integrity and access controls must be enforced. |
| A.8.16 | Monitoring Activities | Monitor networks and systems for anomalous activity | NON-COMPLIANT | No security monitoring or alerting. No SIEM or IDS/IPS deployed. | SIEM with alerting rules must be deployed. Network monitoring and anomaly detection required. |
| A.8.17 | Clock Synchronization | Synchronize system clocks for audit integrity | NON-COMPLIANT | No documented NTP configuration. Log timestamps may be unreliable for forensic use. | NTP must be configured on all systems to ensure accurate, auditable log timestamps. |
| A.8.18 | Use of Privileged Utility Programs | Control use of privileged utility programs | NON-COMPLIANT | No controls on use of admin tools (e.g., cloud CLI, DB admin, network tools). | Use of privileged utilities must be restricted, logged, and approved per the PAM policy. |
| A.8.19 | Installation of Software on Operational Systems | Control software installation on systems | NON-COMPLIANT | No software installation policy. Developers may install unauthorized tools on company devices. | Software allowlist policy and MDM enforcement must be implemented. |
| A.8.20 | Networks Security | Secure networks and prevent unauthorized access | NON-COMPLIANT | No network security architecture documentation. No segmentation between internal and production. | Network security design including segmentation, firewall rules, and DMZ must be documented. |
| A.8.21 | Security of Network Services | Secure network services including cloud and third-party | PARTIAL | Cloud provider manages base network security. PayFlow has not defined additional controls. | PayFlow-specific network security controls (WAF, API gateway, DDoS protection) must be configured. |
| A.8.22 | Segregation of Networks | Segregate networks for different security levels | NON-COMPLIANT | No network segmentation. Dev, staging, and production share the same logical network space. | Network segmentation must be implemented to isolate production from development environments. |
| A.8.23 | Web Filtering | Implement web filtering controls | NON-COMPLIANT | No web filtering or content inspection controls. | DNS-based web filtering must be deployed to block malicious sites and reduce phishing risk. |
| A.8.24 | Use of Cryptography | Define and implement cryptographic controls | PARTIAL | Encryption used in some areas. No consistent cryptographic policy across all systems. | Cryptographic standards policy (algorithms, key lengths, key management) must be documented. |
| A.8.25 | Secure Development Life Cycle | Apply security requirements to the development lifecycle | NON-COMPLIANT | No secure SDLC process. No security testing in CI/CD pipeline. | Secure SDLC must be defined including security requirements, code review, and SAST/DAST tooling. |
| A.8.26 | Application Security Requirements | Define security requirements for applications | NON-COMPLIANT | No security requirements defined for new features or integrations. APIs lack documented security specs. | Application security requirements (OWASP Top 10 coverage) must be defined and enforced. |
| A.8.27 | Secure System Architecture and Engineering Principles | Apply secure engineering principles | NON-COMPLIANT | No secure design principles or threat modelling process documented. | Secure by design principles and threat modelling must be embedded into the architecture process. |
| A.8.28 | Secure Coding | Apply secure coding practices | NON-COMPLIANT | No secure coding guidelines. No mandatory code review process or SAST tooling. | Secure coding standards and mandatory peer code review must be implemented. |
| A.8.29 | Security Testing in Development and Acceptance | Perform security testing before release | NON-COMPLIANT | No security testing in CI/CD pipeline. No UAT security gate. | SAST, DAST, and dependency scanning must be integrated into the CI/CD pipeline. |
| A.8.30 | Outsourced Development | Manage security risks of outsourced development | N/A | Development is currently in-house. | N/A — Review if outsourcing is adopted in future. Secure coding requirements apply to contractors. |
| A.8.31 | Separation of Development, Test and Production | Separate dev, test, and production environments | NON-COMPLIANT | No environment separation. Developers have access to production. Shared credentials observed. | Strict separation of dev/test/prod must be enforced. No sharing of credentials between environments. |
| A.8.32 | Change Management | Manage changes to information processing facilities | NON-COMPLIANT | No formal change management. Developers push directly to production without review. | Change management policy and approval process must be enforced before any production change. |
| A.8.33 | Test Information | Protect test information | NON-COMPLIANT | Real customer PII may be used in testing environments without masking. | Test data management policy must mandate synthetic or masked data for all non-production testing. |
| A.8.34 | Protection of Information Systems During Audit Testing | Protect systems during audits | PARTIAL | No active audit testing capability yet. Audit simulation (Wk 5) will need to be planned carefully. | Audit testing rules of engagement must be defined to prevent unintended disruption. |
