# Mock-VendorSecurityRiskAssessmentReport
A risk-based vendor due diligence framework for evaluating data processors against GDPR, CCPA, and security control requirements using standardized compliance assessment methodology.

By Ramyar Daneshgar 

**Company:** `SecurityEngineer.com`  
**Vendor Evaluated:** `Acme Cloud Services`  
**Assessed by:** Ramyar Daneshgar  
**Date:** April 7, 2025  
**Status:**  High Risk (Remediation Required)

---

## 1. Vendor Overview

```markdown
| Attribute            | Value                                   |
|----------------------|------------------------------------------|
| Legal Entity         | Acme Cloud Services, Inc.                |
| Service Description  | Cloud-based file storage and collaboration |
| Data Handled         | PII, Client Financial Records            |
| Data Processing Role | Processor                                |
| Hosting Location     | United States, Germany                   |
| Third-Party Subprocessors | AWS, Cloudflare, Mixpanel             |
| Contact for Privacy  | privacy@acmecloud.com                    |
```

In this section, I captured **basic vendor information** to establish context. I always start by confirming the legal entity name because it's essential for contracts like a DPA (Data Processing Agreement). Knowing what service they provide tells me what **types of data** may be involved and how mission-critical it is to our business.

In this case, Acme is a **cloud storage provider**, so I flagged them as handling **high-risk data types** — including PII and financial records. Because they process data *on our behalf*, they qualify as a **data processor** under GDPR, and that means **I'm responsible for ensuring we have a DPA in place**.

The hosting location is also critical. Since they host in **Germany**, I know there are **EU data protection obligations** involved — which means I’ll need to check for SCCs (Standard Contractual Clauses) or another compliant transfer mechanism for any data flowing outside the EU.

Lastly, I documented their **subprocessors**, which is important for transparency and accountability under GDPR Article 28(2).

---

## 2. Privacy & Compliance Review

```markdown
| Control Area                     | Finding                                        | Status     |
|----------------------------------|------------------------------------------------|------------|
| GDPR Article 28 DPA Signed       | Not provided                                   | Missing |
| Subprocessor Disclosure          | Incomplete list                                | Partial |
| Data Transfer Safeguards (EEA)   | No SCCs or adequacy provided                   | Missing |
| Data Retention Policy            | Retains logs for 5+ years                      | High Risk |
| Right to Erasure Mechanism       | Manual deletion by support only                | Weak |
| Consent Management (if required) | Not applicable (processor role)                | Pass |
| Privacy Policy Review            | Outdated (last updated 2021)                   | Outdated |
| Security Certifications          | No SOC 2 or ISO 27001                          | Missing |
```


I performed a **control-based assessment** to evaluate how the vendor aligns with core privacy and security obligations. This isn’t just a checkbox exercise — each control here maps to a real legal or framework requirement.

- **DPA**: Since they’re a processor, I verified whether they had a signed DPA. They didn’t — that’s a **critical GDPR violation**.
- **Subprocessor list**: Their website listed a few subprocessors, but the list was outdated and incomplete. Under GDPR, vendors are required to **fully disclose** all subprocessors. 
- **SCCs**: Given their Germany-based operations and U.S. affiliations, I checked for **data transfer mechanisms**. They didn’t provide SCCs, which is required under **Chapter V of GDPR**.
- **Retention policy**: Keeping logs for 5+ years is an issue unless justified (e.g., for legal archiving). Since that wasn't clear.
- **Erasure mechanism**: The “Right to be Forgotten” (GDPR Art. 17) should be easily exercised. If deletion only happens manually by support staff, that’s weak and error-prone.
- **Consent**: They don’t collect data directly from users, so GDPR consent obligations don’t apply.
- **Privacy Policy**: It hadn’t been updated since 2021 — a red flag because policies must reflect **current processing activities**.
- **Certifications**: They had no SOC 2 or ISO 27001 — which I usually expect for any vendor handling sensitive client data.

---

## 3. Risk Scoring

```markdown
| Factor                              | Weight | Score (0-3) |
|-------------------------------------|--------|-------------|
| Data Sensitivity                    | 25%    | 3 (PII + Financial) |
| Volume of Records                   | 15%    | 2            |
| Security Certifications             | 20%    | 0 (None)     |
| Geographic Risk (Data Transfer)     | 15%    | 1            |
| Policy Maturity                     | 10%    | 1            |
| Regulatory Exposure (GDPR/CCPA)     | 15%    | 2            |

**Total Weighted Score:** `1.85 / 3.0`  
**Risk Level:**  High Risk
```

After the qualitative review, I applied a **quantitative risk scoring model**. This gives me a consistent and defensible way to compare vendors — especially useful when justifying my decisions to leadership or audit.

- I weighted **data sensitivity** most heavily, because if this vendor gets breached, we’re exposed to legal and reputational risk.
- They got a **zero** on certifications because they don’t hold any third-party validations — that alone pushed their score down significantly.
- The **data transfer risk** (EU to U.S. without safeguards) was another major concern.
- Policy maturity (outdated privacy docs) was weak, and they scored low on regulatory exposure because they touch both **GDPR** and **CCPA**-regulated data.

The final weighted score: `1.85 / 3` → I round this up to **High Risk**. This means we should not onboard them until the key issues are addressed.

---

## 4. Recommendations

```markdown
1. **Execute a GDPR-compliant Data Processing Agreement (DPA)** prior to onboarding.
2. **Disclose all subprocessors** on a public-facing webpage or provide internal documentation.
3. **Implement Standard Contractual Clauses (SCCs)** for cross-border transfers involving the EEA.
4. **Revise the privacy policy** to reflect current practices, especially data sharing and retention.
5. **Reduce log retention** to under 2 years unless legally required.
6. **Pursue SOC 2 Type II or ISO 27001** certification to demonstrate baseline security controls.
```

Here I documented the **actionable steps** the vendor must take. These recommendations tie directly back to my findings. I don’t just highlight the problems — I offer a roadmap for how the vendor can resolve each one.

- **DPA**: Legal must be involved. No vendor should go live without it.
- **Subprocessors**: Must be transparent. This is a non-negotiable item under GDPR.
- **SCCs**: Absolutely necessary for international data transfers — especially post-Schrems II ruling.
- **Policy revision**: This is low-effort but necessary to demonstrate accountability.
- **Retention**: Shortening data retention reduces legal exposure and aligns with **data minimization principles**.
- **Certifications**: While not mandatory, achieving SOC 2 or ISO 27001 shows the vendor is maturing and invests in its security program.

---

## 5. Final Recommendation

```markdown
> Do not proceed with vendor onboarding until critical privacy and security gaps are addressed:
> - Signed Data Processing Agreement (DPA)
> - Documented subprocessors
> - Data transfer safeguards (SCCs)

---

Signed:  
Ramyar Daneshgar  
_Compliance & Privacy Analyst_  
2025-04-07
```


Finally, I made a **formal recommendation** based on the findings and scoring. This is essential for documentation and accountability. If a business team wants to proceed anyway, they’ll need to **formally accept the risk** — and that risk is now logged and traceable.

By signing and dating the report, I’m taking ownership of my risk assessment — and leaving a clear audit trail.
