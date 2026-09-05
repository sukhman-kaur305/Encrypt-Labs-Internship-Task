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
- Its own `README.md` where relevant, summarizing the objective and findings

## Task index

| Week | Task | Title | Skill Domain | Status |
|------|------|-------|---------------|--------|
| 1 | 1 | *(add title)* | | |
| 1 | 2 | *(add title)* | | |
| 1 | 3 | *(add title)* | | |
| 1 | 4 | *(add title)* | | |
| 2 | 1 | *(add title)* | | |
| ... | | | | |
| — | — | IAM Privilege Escalation Path Analysis and Risk Mitigation | IAM / Cloud Privilege Escalation | Complete |
| — | — | AWS STS Assume-Role Abuse Scenarios and Trust Policy Hardening | IAM / Security Token Service (STS) | Complete |
| — | — | Capstone: End-to-End AWS Cloud Security Assessment (flaws.cloud L1–6) | S3, IAM, EC2/EBS, IMDS, Lambda/API Gateway | In progress |

*(Fill in week/task numbers above to match your actual folder layout as you go — the last three rows are the tasks already completed and are placed once their week/task numbers are confirmed.)*

## Tools & frameworks used across tasks

- **AWS CLI v2, IAM Policy Simulator, IAM Access Analyzer**
- **CloudGoat**, **IAM Vulnerable**, **flaws.cloud** — intentionally vulnerable lab environments
- **Cloudsplaining**, **PMapper / Principal Mapper** — IAM policy and privilege-escalation analysis
- **gitleaks** — secret scanning before every commit
- **MITRE ATT&CK**, **NIST SP 800-53**, **ISO 27001**, **CIS Controls**, **OWASP Cloud Top 10** — guiding frameworks referenced in findings and remediation

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

## License

*(Optional — add a license here, e.g. MIT, if you want others to be able to reuse the write-ups, or state "All rights reserved" if not.)*
