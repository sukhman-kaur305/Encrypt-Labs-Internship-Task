# Encrypt Labs — Junior Cloud Security Engineer Internship

Task submissions and evidence for the **EncryptEdge Labs Junior Cloud
Security Engineer Internship Programme**, organized by week. Each task
focuses on a specific cloud security skill — IAM, AWS STS, S3, EC2/EBS,
and end-to-end attack-chain analysis — using isolated sandbox accounts
and intentionally vulnerable lab environments (CloudGoat, flaws.cloud,
IAM Vulnerable, Cybr, PwnedLabs).

**Author:** [sukhman-kaur305](https://github.com/sukhman-kaur305)

---

## Repository structure

```
Encrypt-Labs-Internship-Task/
├── README.md
├── week1/
│   ├── task1/
│   ├── task2/
│   ├── task3/
│   └── task4/
├── week2/
│   └── ...
...
└── week8/
    └── task4/
```

Each `taskN/` folder is self-contained and typically includes:
- A final report (PDF or Markdown)
- An `evidence/` subfolder with command logs, screenshots, and JSON/config artifacts

## Task index

| Week | Task | Task ID | Title | Skill Domain | Status |
|------|------|---------|-------|---------------|--------|
| 1 | 1 | CSE-AWS-T001 | Cloud Security Foundations & AWS Shared Responsibility Model | Shared Responsibility Model / IAM, S3, EC2, CloudTrail Risk Mapping | Not started |
| 1 | 2 | CSE-AWS-L-002-04 | AWS Account Hardening and Secure Cloud Security Homelab Setup | Account Hardening / MFA / CloudTrail, Config, GuardDuty / CloudGoat & iam-vulnerable | Complete |
| 1 | 3 | CSE-AWS-L-003-04 | Secure AWS CLI Configuration and Identity-Based Access Operations | IAM / AWS CLI Profiles / Least Privilege / Temporary Credentials & MFA | Complete |
| 1 | 4 | | Cloud Threat Modeling and Attack Surface Identification in AWS | Threat Modeling / Attack Surface (STRIDE + MITRE ATT&CK) | Complete |
| 2 | 1 | | AWS Identity and Access Management Architecture and Security Design | IAM Architecture / Trust Relationships | Complete |
| 2 | 2 | | *(add title)* | | |
| 2 | 3 | | AWS IAM Enumeration, Access Mapping and Risk Analysis | IAM Enumeration / Privilege Mapping | Complete |
| 2 | 4 | | AWS IAM Credential Audit, Key Rotation and Identity Risk Assessment | Credential Auditing / Key Rotation | Complete |
| 2 | 5 | | Least-Privilege IAM Policy Engineering and Permission Boundary Implementation | IAM Least Privilege / Permission Boundaries | Complete |
| 3 | 1 | | Amazon S3 Architecture, Access Control and Data Protection | S3 / Access Control / Encryption | Complete |
| 3 | 2 | | Secure Amazon S3 Configuration, Encryption and Access Control | S3 / SSE-KMS / Versioning / Logging | Complete |
| 3 | 3 | CSE-AWS-L-011-04 | Amazon S3 Exposure Detection, Policy Analysis, and Access Enumeration | S3 Enumeration / Policy Analysis | Complete |
| 3 | 4 | | S3 Misconfiguration Exploitation, Remediation and Hardening | S3 Exploitation / Remediation / Hardening | Complete |
| ... | | | | | |
| 4 | 1 | | AWS Credential Types, Secret Discovery and Lifecycle Security | Credential Management / Secret Scanning | Complete |
| 4 | 2 | | AWS Secrets Manager, Least-Privilege IAM and Lambda Integration | Secrets Manager / IAM Least Privilege | Complete |
| 4 | 3 | | AWS Secrets Rotation, KMS Encryption, Auditing and Governance | KMS / CloudTrail Auditing / Governance | Complete |
| 4 | 4 | | Cloud Credential Exposure Detection, Incident Response and Rotation | Secret Scanning / Incident Response | Complete |
| 5 | 1 | | Amazon EC2 Identity, Metadata Service and Secure Instance Access | EC2 / IMDSv2 / IAM Instance Profiles | Complete |
| 5 | 2 | | EC2 Credential Compromise Detection, Containment and Incident Response | GuardDuty / CloudTrail / Incident Response | Complete |
| 5 | 3 | | AWS Lambda Security Architecture, Permissions and Event-Driven Threat Modeling | Lambda / Event-Driven IAM / STRIDE Modeling | Complete |
| 6 | 1 | | AWS CloudTrail Security Monitoring, Event Analysis and Log Integrity | CloudTrail / Log Integrity / Event Analysis | Complete |
| 6 | 2 | | IAM and S3 Anomaly Detection Using AWS CloudTrail | Anomaly Detection / Athena / CloudWatch | Complete |
| 6 | 3 | | AWS Cloud Incident Response: Detection, Containment, Eradication & Recovery | Incident Response / GuardDuty / EventBridge & Lambda Automation | Complete |
| 6 | 4 | | Manual AWS Security Posture Review and Risk Assessment | Manual Security Review / IAM, S3, EC2, CloudTrail | Complete |
| 7 | 1 | | AWS IAM Enumeration, Weak Credentials & Policy Misconfiguration Analysis | IAM Enumeration / Weak Credentials / iam-vulnerable | Complete |
| 7 | 2 | | AWS IAM Privilege Escalation Path Analysis & Mitigation | IAM / Cloud Privilege Escalation | Complete |
| 7 | 3 | | AWS STS AssumeRole Abuse, Role Chaining & Trust Policy Hardening | IAM / Security Token Service (STS) | Complete |
| 7 | 4 | | AWS Multi-Service Enumeration, Correlation & Risk Prioritization | Multi-Service Enumeration / IAM, S3, EC2, Lambda / Risk Prioritization | Complete |
| 8 | 1 | CSE-AWS-P-029-08 | Capstone: End-to-End AWS Cloud Security Assessment (flaws.cloud L1–6) | S3, IAM, EC2/EBS, IMDS, Lambda/API Gateway | In progress |

*(Fill in week/task numbers above to match your actual folder layout as you go. `CSE-AWS-T001` is assumed to be Week 1 / Task 1 as the introductory foundations task — adjust if your folder layout differs. Weeks 6–8 task titles are taken directly from their task-brief headers; add Task IDs for those once assigned.)*

## Tools & frameworks used across tasks

- **AWS CLI v2, IAM Policy Simulator, IAM Access Analyzer**
- **CloudGoat**, **IAM Vulnerable**, **flaws.cloud** — intentionally vulnerable lab environments
- **Cloudsplaining**, **PMapper / Principal Mapper**, **Policy Sentry** — IAM policy and privilege-escalation analysis
- **TruffleHog**, **gitleaks** — secret scanning before every commit
- **AWS Secrets Manager, KMS, GuardDuty, Security Hub, CloudTrail/CloudWatch, Athena** — secrets lifecycle, credential auditing, and detection tooling
- **Steampipe**, **jq**, **Terraform**, **Burp Suite Community Edition** — S3/IAM enumeration, policy analysis, and exploitation/remediation testing
- **OWASP Threat Dragon**, **OWASP PyTM** — structured threat model diagramming and automated threat modeling
- **MITRE ATT&CK**, **NIST SP 800-53 / 800-61r2 / 800-57 / 800-30**, **ISO 27001**, **CIS Controls / CIS AWS Foundations Benchmark**, **OWASP Cloud Top 10 / Serverless Top 10**, **SFIA**, **NICE Framework** — guiding frameworks referenced in findings and remediation

## Evidence handling & redaction practice

All evidence in this repository has been reviewed and sanitized before
being committed:

- No full AWS Access Key IDs, Secret Access Keys, or session tokens
- No full 12-digit AWS account IDs (redacted or replaced with placeholder values, e.g. `111111111111`)
- No personal names or email addresses in report front matter or signature blocks
- No real hostnames/usernames in terminal screenshots
- Every commit is scanned with `gitleaks` before pushing; see `.gitleaks.toml` for the allowlist covering known false positives (e.g. reports that document an already-redacted finding)

All lab activity was performed exclusively in isolated, authorized
sandbox accounts and intentionally vulnerable training environments —
no production systems, third-party accounts, or real customer data were
ever accessed.

