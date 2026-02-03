# Botium Toys Security Audit

**Author:** Dariusz Piasecki  
**Project Type:** Internal IT Security Audit & Risk Assessment  
**Framework:** NIST Cybersecurity Framework (CSF)

---

## 📋 Executive Summary

This project documents a comprehensive internal security audit conducted for **Botium Toys**, a small U.S.-based toy manufacturer and retailer. The audit was performed using the **NIST Cybersecurity Framework** to assess the company's security posture, identify vulnerabilities, and ensure compliance with industry regulations (PCI DSS, GDPR, SOC).

**Key Findings:**
- **Risk Score:** 8/10 (High) due to inadequate asset management and missing critical controls
- **11 out of 14 controls** require immediate implementation
- **Critical gaps** in data encryption, access control, and disaster recovery
- **Compliance deficiencies** across PCI DSS, GDPR, and SOC standards

**Outcome:** Delivered actionable recommendations to reduce risk, improve security posture, and achieve regulatory compliance.

---

## 🏢 Company Background

### Botium Toys Overview

**Industry:** Toy Manufacturing & Retail  
**Size:** Small Business  
**Operations:**
- Single physical location (office, storefront, warehouse)
- Growing online presence (U.S. and international customers)
- Expanding IT infrastructure under pressure to support global market

**Business Challenge:**
The IT department lacks a clear plan to maintain compliance and secure operations as the company scales. The manager identified the need for an internal audit to:
- Identify and mitigate risks, threats, and vulnerabilities
- Ensure compliance with payment processing regulations (PCI DSS)
- Meet EU data protection requirements (GDPR)

---

## 🎯 Audit Scope and Goals

### Scope

The audit encompasses the **entire security program** at Botium Toys, including:

| Category | Assets Covered |
|----------|----------------|
| **Physical Assets** | Employee equipment (desktops, laptops, smartphones), surveillance cameras, storefront/warehouse inventory |
| **Network Infrastructure** | Internal network, internet access, legacy systems |
| **Systems & Software** | Accounting, telecom, database, security, e-commerce, inventory management |
| **Data** | Customer PII/SPII, payment card data, retention and storage systems |

### Goals

1. **Assess existing assets** managed by the IT department
2. **Complete controls and compliance checklists** to identify gaps
3. **Determine which controls** need implementation to improve security posture
4. **Provide actionable recommendations** to reduce risk and ensure compliance

---

## 🔍 Risk Assessment

### Risk Description

**Current State:**
- Inadequate asset management
- Missing critical security controls
- Non-compliance with U.S. and international regulations (PCI DSS, GDPR, SOC)

### Risk Score

**8 out of 10** (High Risk)

**Justification:**
- Lack of preventative, detective, and corrective controls
- Insufficient adherence to compliance best practices
- Potential for significant financial and reputational damage

### Impact Analysis

| Risk Category | Impact Level | Description |
|---------------|--------------|-------------|
| **Asset Loss** | Medium | IT department lacks visibility into which assets are at risk |
| **Regulatory Fines** | High | Non-compliance with PCI DSS, GDPR could result in substantial penalties |
| **Data Breach** | High | Lack of encryption and access controls exposes customer PII/payment data |
| **Business Continuity** | High | No disaster recovery plan or data backups in place |

---

## 🚨 Critical Findings

### Security Vulnerabilities Identified

| #  | Vulnerability | Severity | Details |
|----|---------------|----------|---------|
| 1  | **Unrestricted Data Access** | 🔴 Critical | All employees can access cardholder data and customer PII/SPII |
| 2  | **No Data Encryption** | 🔴 Critical | Credit card data stored in plaintext in internal database |
| 3  | **Missing Access Controls** | 🔴 Critical | No least privilege or separation of duties policies |
| 4  | **No Disaster Recovery Plan** | 🔴 Critical | Company has no backups of critical data |
| 5  | **No Intrusion Detection** | 🟡 High | No IDS installed to detect anomalous traffic |
| 6  | **Weak Password Policy** | 🟡 High | Minimal requirements (not aligned with current standards) |
| 7  | **No Password Management System** | 🟡 High | Manual password resets affect productivity |
| 8  | **Unscheduled Legacy System Maintenance** | 🟡 High | No regular maintenance schedule or clear intervention methods |

---

## 📊 Controls Assessment

### Control Implementation Status

| Control Category | Implemented | Missing | Total |
|------------------|-------------|---------|-------|
| **Administrative** | 1 | 4 | 5 |
| **Technical** | 2 | 5 | 7 |
| **Physical** | 3 | 0 | 3 |
| **TOTAL** | **6** | **9** | **15** |

---

### Detailed Controls Checklist

#### ✅ Controls Currently in Place

| Control Name | Type | Category | Purpose |
|-------------|------|----------|---------|
| Firewall | Preventative | Technical | Filters malicious traffic based on security rules |
| Antivirus Software | Preventative | Technical | Scans and quarantines known threats |
| CCTV Surveillance | Preventative/Detective | Physical | Monitors and records physical premises |
| Locks (offices, storefront, warehouse) | Deterrent/Preventative | Physical | Prevents unauthorized physical access |
| Fire Detection/Prevention | Detective/Preventative | Physical | Detects fire and prevents damage to assets |
| Manual Monitoring (Legacy Systems) | Preventative | Technical | Manages out-of-date systems (ad-hoc) |

---

#### ❌ Controls That Need Implementation

| Control Name | Type | Category | Priority | Impact |
|-------------|------|----------|----------|--------|
| **Least Privilege** | Preventative | Administrative | 🔴 Critical | Reduces risk from malicious insiders/compromised accounts |
| **Disaster Recovery Plans** | Corrective | Administrative | 🔴 Critical | Ensures business continuity after incidents |
| **Encryption** | Deterrent | Technical | 🔴 Critical | Protects confidentiality of sensitive data (PCI DSS) |
| **Backups** | Corrective | Technical | 🔴 Critical | Enables recovery from data loss events |
| **Password Policies** | Preventative | Administrative | 🟡 High | Reduces account compromise via brute-force |
| **Separation of Duties** | Preventative | Administrative | 🟡 High | Limits impact from compromised accounts |
| **IDS/IPS** | Detective | Technical | 🟡 High | Detects anomalous traffic matching threat signatures |
| **Password Management System** | Preventative | Technical | 🟡 High | Enforces complexity requirements, reduces fatigue |
| **Account Management Policies** | Preventative | Administrative | 🟢 Medium | Manages account lifecycle, limits attack surface |

---

## 📜 Compliance Assessment

### Regulatory Standards Evaluated

#### 1. Payment Card Industry Data Security Standard (PCI DSS)

**Status:** ❌ **Non-Compliant** (0 out of 4 requirements met)

| Requirement | Status | Gap Identified |
|-------------|--------|----------------|
| Only authorized users access credit card data | ❌ | All employees have access |
| Secure environment for card data | ❌ | Data stored in plaintext in internal database |
| Data encryption for transactions | ❌ | No encryption implemented |
| Secure password management | ❌ | Weak policy, no management system |

**Risk:** Potential fines up to **$500,000 per incident** + loss of payment processing privileges.

---

#### 2. General Data Protection Regulation (GDPR)

**Status:** ⚠️ **Partially Compliant** (2 out of 4 requirements met)

| Requirement | Status | Gap Identified |
|-------------|--------|----------------|
| EU customers' data is private/secured | ❌ | No encryption, unrestricted access |
| 72-hour breach notification plan | ✅ | Plan established |
| Data classification and inventory | ❌ | Assets not properly classified |
| Privacy policies enforced | ✅ | Policies developed and enforced |

**Risk:** Fines up to **€20 million or 4% of annual global turnover** (whichever is higher).

---

#### 3. System and Organizations Controls (SOC type 1, SOC type 2)

**Status:** ⚠️ **Partially Compliant** (2 out of 4 requirements met)

| Requirement | Status | Gap Identified |
|-------------|--------|----------------|
| User access policies established | ❌ | No least privilege or separation of duties |
| PII/SPII confidentiality | ❌ | All employees can access sensitive data |
| Data integrity | ✅ | Controls ensure consistency and accuracy |
| Data availability | ✅ | Authorized access ensured |

**Risk:** Loss of customer trust, failed audits, inability to secure enterprise contracts.

---

## 💡 Recommendations

### Priority 1: Critical (Implement Immediately)

| # | Recommendation | Expected Outcome | Implementation Timeline |
|---|----------------|------------------|-------------------------|
| 1 | **Implement Least Privilege Access Control** | Only authorized personnel access sensitive data | 2-4 weeks |
| 2 | **Deploy Data Encryption** (AES-256) | PCI DSS compliance, protect cardholder data | 4-6 weeks |
| 3 | **Establish Disaster Recovery Plan** | Business continuity, data recovery capability | 4-8 weeks |
| 4 | **Implement Automated Backups** | Daily backups with 3-2-1 strategy | 2-3 weeks |

---

### Priority 2: High (Implement Within 90 Days)

| # | Recommendation | Expected Outcome | Implementation Timeline |
|---|----------------|------------------|-------------------------|
| 5 | **Install Intrusion Detection System (IDS)** | Real-time threat detection | 3-4 weeks |
| 6 | **Strengthen Password Policy** (12+ chars, complexity) | Reduce brute-force risk | 1-2 weeks |
| 7 | **Deploy Password Management System** | Enforce policy, reduce IT tickets | 2-3 weeks |
| 8 | **Implement Separation of Duties** | Limit insider threat impact | 3-6 weeks |

---

### Priority 3: Medium (Implement Within 6 Months)

| # | Recommendation | Expected Outcome | Implementation Timeline |
|---|----------------|------------------|-------------------------|
| 9 | **Establish Legacy System Maintenance Schedule** | Predictable updates, clear procedures | 2-4 weeks |
| 10 | **Deploy Account Management Policies** | Lifecycle management, reduced attack surface | 4-6 weeks |
| 11 | **Conduct Asset Classification & Inventory** | GDPR compliance, risk visibility | 6-8 weeks |

---

## 📈 Expected Impact

### Risk Reduction

| Metric | Before Audit | After Implementation | Improvement |
|--------|--------------|----------------------|-------------|
| **Risk Score** | 8/10 (High) | 3/10 (Low) | **-62.5%** |
| **Controls Implemented** | 6/15 (40%) | 15/15 (100%) | **+60%** |
| **PCI DSS Compliance** | 0/4 (0%) | 4/4 (100%) | **+100%** |
| **GDPR Compliance** | 2/4 (50%) | 4/4 (100%) | **+50%** |
| **SOC Compliance** | 2/4 (50%) | 4/4 (100%) | **+50%** |

---

### Business Benefits

✅ **Avoid Regulatory Fines:** PCI DSS and GDPR penalties can exceed millions of dollars  
✅ **Protect Customer Trust:** Secure handling of payment and personal data  
✅ **Enable Business Growth:** Compliance unlocks enterprise contracts and EU market expansion  
✅ **Reduce Incident Response Costs:** Proactive controls prevent expensive breaches  
✅ **Improve Operational Efficiency:** Automated systems reduce manual password resets  

---

## 🛠️ Tools & Frameworks

| Category | Tool/Framework | Purpose |
|----------|----------------|---------|
| **Framework** | NIST Cybersecurity Framework (CSF) | Structured approach to security audit |
| **Standards** | PCI DSS 3.2.1 | Payment card data security |
| **Standards** | GDPR (EU 2016/679) | EU customer data protection |
| **Standards** | SOC 2 Type II | Security, availability, confidentiality controls |
| **Methodology** | Risk Assessment Matrix | Prioritize vulnerabilities by impact and likelihood |

---

## 📂 Project Deliverables

This audit produced the following documentation:

1. **Scope and Goals Statement** – Defines audit boundaries and objectives
2. **Asset Inventory** – Complete list of IT-managed assets
3. **Risk Assessment Report** – Risk score, impact analysis, and vulnerability details
4. **Controls Assessment Checklist** – 15 controls evaluated (6 implemented, 9 missing)
5. **Compliance Checklist** – PCI DSS, GDPR, SOC evaluation
6. **Recommendations Report** – Prioritized action plan with timelines

---

## 🎯 Skills Demonstrated

| Skill Category | Specific Skills |
|----------------|-----------------|
| **Security Auditing** | Internal audit planning, scope definition, risk assessment |
| **Framework Application** | NIST CSF implementation, control categorization |
| **Compliance** | PCI DSS, GDPR, SOC 2 requirements analysis |
| **Risk Management** | Vulnerability identification, risk scoring, impact analysis |
| **Technical Documentation** | Security reports, checklists, recommendations |
| **Strategic Thinking** | Prioritization, cost-benefit analysis, business continuity planning |

---

## 📝 Lessons Learned

### Key Takeaways

1. **Small businesses often lack basic security controls** due to resource constraints and rapid growth
2. **Compliance is not optional** – regulatory fines can devastate small companies
3. **Risk assessment must precede control implementation** to ensure resources are allocated effectively
4. **Defense in depth requires multiple control layers** (administrative, technical, physical)
5. **Business continuity planning is critical** – no backups = no recovery from incidents

### Challenges Addressed

- **Limited Budget:** Prioritized controls by risk and compliance impact
- **Growing Business:** Recommendations scaled with company growth trajectory
- **International Operations:** Ensured GDPR compliance for EU customers
- **Legacy Systems:** Defined maintenance schedule without disrupting operations

---

## 🔗 Related Projects

- [SQL Security Analysis](../sql-security-analysis) – Database investigation and threat detection
- Network Security Configuration (Coming Soon)
- Incident Response Playbook (Coming Soon)

---

## 📧 Contact

**Dariusz Piasecki**  
📧 Email: dariusz.piasecki.sec@gmail.com  
🔗 LinkedIn: [linkedin.com/in/piaseckiphotos](https://linkedin.com/in/piaseckiphotos)  
🐙 GitHub: [github.com/Dariusz-Piasecki](https://github.com/Dariusz-Piasecki)

---

*This security audit demonstrates practical application of the NIST Cybersecurity Framework to assess organizational risk, evaluate controls, and ensure regulatory compliance in a real-world business context.*
