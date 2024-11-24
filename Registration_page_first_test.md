# ZAP by Checkmarx Scanning Report

Generated with [ZAP](https://zaproxy.org) ![The ZAP logo](Registration_page_first_test/zap32x32.png) on Sun 24 Nov 2024, at 17:49:58  
ZAP Version: 2.15.0  
ZAP by [Checkmarx](https://checkmarx.com/)

---

## Contents

1. [About this report](#about-this-report)
   - [Report parameters](#report-parameters)
2. [Summaries](#summaries)
   - [Alert counts by risk and confidence](#risk-confidence-counts)
   - [Alert counts by site and risk](#site-risk-counts)
   - [Alert counts by alert type](#alert-type-counts)
3. [Alerts](#alerts)
4. [Appendix](#appendix)
   - [Alert types](#alert-types)

---

## About this report

### Report parameters

#### Contexts

No contexts were selected, so all contexts were included by default.

#### Sites

The following sites were included:

- `http://localhost:8000`

#### Risk levels

**Included:** High, Medium, Low, Informational  
**Excluded:** None

#### Confidence levels

**Included:** User Confirmed, High, Medium, Low  
**Excluded:** User Confirmed, High, Medium, Low, False Positive

---

## Summaries

### Alert counts by risk and confidence

| Risk / Confidence | User Confirmed | High | Medium | Low | Total |
| ----------------- | -------------- | ---- | ------ | --- | ----- |
| High              | 0              | 0    | 1      | 1   | 2     |
| Medium            | 0              | 1    | 1      | 0   | 2     |
| Low               | 0              | 0    | 1      | 0   | 1     |
| Informational     | 0              | 0    | 1      | 0   | 1     |
| **Total**         | 0              | 1    | 4      | 1   | 6     |

---

### Alert counts by site and risk

| Site                    | High | Medium | Low | Informational |
| ----------------------- | ---- | ------ | --- | ------------- |
| `http://localhost:8000` | 2    | 2      | 1   | 1             |

---

### Alert counts by alert type

| Alert type                                   | Risk          | Count |
| -------------------------------------------- | ------------- | ----- |
| Path Traversal                               | High          | 1     |
| SQL Injection                                | High          | 1     |
| Content Security Policy (CSP) Header Not Set | Medium        | 1     |
| Missing Anti-clickjacking Header             | Medium        | 1     |
| X-Content-Type-Options Header Missing        | Low           | 2     |
| User Agent Fuzzer                            | Informational | 12    |

---

## Alerts

### High Risk

- **[SQL Injection](#alert-type-1)** (1 alert on `http://localhost:8000`)

### Medium Risk

- **[Content Security Policy (CSP) Header Not Set](#alert-type-2)** (1 alert on `http://localhost:8000`)

---

## Appendix

### Alert Types

#### Path Traversal

- CWE ID: [22](https://cwe.mitre.org/data/definitions/22.html)

#### SQL Injection

- CWE ID: [89](https://cwe.mitre.org/data/definitions/89.html)

#### Content Security Policy (CSP) Header Not Set

- CWE ID: [693](https://cwe.mitre.org/data/definitions/693.html)

---
