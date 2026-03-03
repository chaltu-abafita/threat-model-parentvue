# 🔐 Threat Modeling: Bellevue School District ParentVUE System

## 📌 Overview
This project presents a comprehensive **threat model and risk assessment** for the  
**Bellevue School District (BSD) ParentVUE System**, a web and mobile platform used by parents, teachers, and administrators to access sensitive student information.

The system processes **FERPA-protected data**, including academic records, attendance, health information, and secure messaging. A structured threat modeling approach was used to identify risks and recommend mitigations that protect **confidentiality, integrity, and availability (CIA)**.

---

## 🧠 Objectives
- Identify security threats affecting ParentVUE and its backend systems
- Analyze trust boundaries and data flows
- Apply the **STRIDE threat modeling framework**
- Assess risk using a qualitative risk matrix
- Recommend practical, defense-in-depth mitigations

---

## 🏗 System Overview
ParentVUE is a **web and mobile application** integrated with the **Synergy Student Information System (SIS)**. It allows:
- Parents to view grades, attendance, and update student details
- Teachers to enter grades and communicate with families
- Administrators to manage enrollment and student records

The platform operates under a **shared responsibility model** between:
- **Edupoint (Vendor)** – platform hosting, backend services, patches
- **Bellevue School District (BSD)** – identity management, RBAC, internal security, incident response

---

## 👥 Key Stakeholders
- Parents (primary users)
- Teachers
- School Administrators
- BSD IT & Security Teams
- BSD Leadership
- Edupoint (software vendor)
- State Education Agencies

---

## 🔐 Assets Identified
- ParentVUE web portal and mobile applications
- Parent and staff credentials
- Student academic, demographic, and health data
- Attendance and scheduling data
- Synergy Mail messaging system
- District infrastructure and reputation

---

## 🔄 Trust Boundaries & Data Flows
Key trust boundaries include:
- **External boundary**: Parents, teachers, administrators using personal devices
- **Internal district boundary**: Web servers, process servers, databases
- **Vendor boundary**: Edupoint-hosted backend services

Data Flow Diagrams (DFD Level 0 and Level 1) were used to visualize:
- Authentication flows
- Data retrieval and updates
- Messaging operations
- Interactions with the Synergy SIS database

---

## 🧩 Threat Modeling Framework
**STRIDE** was selected to systematically identify threats across:
- Spoofing
- Tampering
- Repudiation
- Information Disclosure
- Denial of Service
- Elevation of Privilege

---

## 🚨 Key STRIDE Findings
**High-Risk Threats**
- Credential theft and account spoofing
- Unauthorized access to student records
- Potential Synergy database compromise

**Medium–High Risks**
- Grade or attendance tampering
- Messaging impersonation
- Authentication denial-of-service attacks

These risks were mapped to affected components, impact, and recommended mitigations.

---

## 📊 Risk Assessment
A qualitative **risk matrix and heat map** were used to prioritize threats based on:
- Likelihood
- Impact on confidentiality, integrity, and availability

**Top Risks Identified**
- Credential theft / account spoofing
- Unauthorized access due to weak RBAC
- Database breach
- Academic record tampering
- Messaging impersonation
- Authentication service disruption

---

## 🛡 Mitigation Summary
Recommended controls include:

**Authentication**
- Multi-factor authentication (MFA)
- Strong password policies
- Account lockout and anomaly detection

**Access Control**
- Role-Based Access Control (RBAC)
- Least privilege enforcement
- Regular access reviews

**Data Protection**
- TLS encryption in transit
- Encryption at rest
- Secure API endpoints

**Integrity & Accountability**
- Input validation
- Message signing
- Audit logging and timestamping

**Availability**
- Rate limiting
- Load balancing
- Resource throttling and queue management

These controls support a **defense-in-depth strategy**.

---

## ✅ Conclusion
This threat model provides a structured, real-world security assessment of a FERPA-regulated education platform. By aligning threats with data flows and trust boundaries, the project delivers **actionable recommendations** to strengthen system security, protect student privacy, and maintain trust between families and the district.

---

## ✍️ Author
**Chaltu Abafita**  
Cybersecurity Student | Software Testing Engineer  

> Copilot supported the writing process.  
> All system analysis, threat modeling, diagrams, and risk evaluation were completed by the author.

---

## 📚 References
- Microsoft Copilot  
- Lucidchart
