# RISK-ASSESSMENT-NIST-800-30
# Operational Risk Assessment: Remote Workforce Access

## 1. Executive Summary
This document outlines a targeted risk assessment conducted for a distributed remote workforce environment under the **NIST SP 800-30** methodology. The objective is to identify, analyze, and establish risk treatment strategies for unsecured remote network connections accessing sensitive enterprise and regulatory data assets (such as HIPAA-regulated environments).

---

## 2. System Characterization & Scope
* **Asset/System:** Remote worker endpoints (laptops) connecting from external networks.
* **Data Context:** Corporate cloud environments, Customer Relationship Management (CRM), and Electronic Health Record (EHR) platforms.
* **Environment Boundary:** Remote telecommuting environments operating outside the direct physical perimeter of the corporate office.

---

## 3. Threat Identification & Vulnerabilities
* **Threat Sources:** 
  * *Adversarial:* External cybercriminals targeting remote access points.
  * *Accidental:* Remote employees utilizing unencrypted public or home networks.
* **Vulnerability Statement:** 
  > *"Because of a lack of forced VPN configuration and absent multi-factor authentication (MFA) enforcement on secondary access vectors, a remote user could connect via an unsecured network, resulting in potential credential capture, interception, or unauthorized data exposure."*

---

## 4. Risk Analysis (Likelihood & Impact Scoring)
Using a qualitative matrix (Low, Medium, High):

* **Likelihood of Occurrence:** **Medium-High**
  * *Justification:* Variable home network security and human behavior outside the physical office increase the probability of accidental exposure if technical boundaries are missing.
* **Magnitude of Impact:** **High**
  * *Justification:* Compromised credentials or intercepted traffic could grant unauthorized external actors access to confidential consumer data and protected health information, risking severe regulatory non-compliance (HIPAA) and operational downtime.
* **Overall Risk Level:** **HIGH**

---

## 5. Risk Treatment & Response Strategy
Because the assessed risk level is evaluated as **High**, management must apply one of the four NIST risk responses. The chosen strategy and corresponding technical controls are outlined below:

| Risk Response Option | Action Implemented / Planned |
| :--- | :--- |
| **1. Mitigate (Remediate)** | • Enforce mandatory, always-on VPN tunnels with managed split-tunneling.<br>• Mandate Multi-Factor Authentication (MFA) across all authentication endpoints.<br>• Implement continuous logging and anomaly monitoring via Active Directory and ServiceNow ITSM tools. |
| **2. Transfer** | • Maintain secondary cyber liability insurance (supplemental, non-primary control). |
| **3. Avoid** | • *Rejected:* Shutting down remote operations entirely is non-viable for business continuity. |
| **4. Accept** | • *Rejected:* Unacceptable residual risk due to mandatory federal regulatory baselines (HIPAA); cannot accept without implementing active technical controls. |

---

## 6. Document Maintenance & Review
* **Review Cycle:** Annual, or immediately following significant infrastructure, policy, or regulatory modifications.
* **Stakeholders:** IT Operations, Security Engineering, and GRC Compliance Teams.
