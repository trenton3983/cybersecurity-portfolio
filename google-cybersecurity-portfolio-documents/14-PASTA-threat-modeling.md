# **PASTA Threat Modeling – Sneaker Shopping App**


## **Stage I – Define Business and Security Objectives**

**Business Objectives:**

- Ensure a seamless platform for connecting sneaker buyers and sellers, supporting efficient listing, searching, and transactions.
- Enable secure user onboarding with account management features such as sign-up, login, and user ratings.
- Implement strong data privacy protections, especially for payment processing, to comply with legal and financial regulations.


## **Stage II – Define the Technical Scope**

**Technologies Used:**

- **API**
- **PKI (AES & RSA)**
- **SHA-256**
- **SQL**

**Prioritized Technology: SQL**

**Reason for Prioritization:**

SQL is critical because it handles storage and retrieval of sneaker listings, user profiles, and transaction records. Improper configuration or lack of sanitization exposes the system to **SQL injection attacks**, which could leak or destroy sensitive data. Prioritizing SQL ensures database queries are secure and validates all inputs effectively.


## **Stage III – Decompose the Application**

**Reviewed Data Flow Diagram:**

- **User** interacts with the app to search for sneakers.
- The **Product search process** queries the **Database** for listings.
- Results are sent back to the user.

**Security Consideration:**

- **AES** and **SHA-256** protect sensitive data in transit and at rest (e.g., login credentials and payment info).
- Secure **API** calls facilitate communication between frontend and backend without exposing internal systems.


## **Stage IV – Threat Analysis**

**Internal Threat:**

- **Insider misuse of database credentials** could expose or alter inventory and user data.

**External Threat:**

- **Session hijacking** via unsecured cookies or poor token handling could allow attackers to impersonate users and access their data.


## **Stage V – Vulnerability Analysis**

**Vulnerabilities:**

- **Lack of prepared statements** in SQL queries could lead to SQL injection attacks.
- **Weak login credentials** (e.g., no complexity requirements) may allow brute-force attacks and unauthorized access.


## **Stage VI – Attack Modeling**

**Attack Tree Insights:**

- Target: **User data**
  - Method 1: **SQL Injection**
    - Exploit: **Lack of prepared statements**
  - Method 2: **Session Hijacking**
    - Exploit: **Weak login credentials**

These attack paths demonstrate how small configuration flaws can lead to serious data breaches.


## **Stage VII – Risk Analysis and Impact**

**Security Controls to Reduce Risk:**

- **Use prepared statements** and parameterized queries to prevent SQL injection.
- **Implement multi-factor authentication (MFA)** to enhance account security.
- **Use secure cookies and HTTPS-only sessions** to defend against session hijacking.
- **Conduct regular code reviews and penetration testing** to discover and fix vulnerabilities before attackers exploit them.

---

# **ChatGPT assessment of the completed PASTA Threat Model** compared to the provided **Exemplar**

[PASTA Threat Modeling Supporting Material]()

## ✅ **Stage I – Define Business and Security Objectives**

### **Your Response:**
- Connect buyers and sellers seamlessly.
- Support secure account features.
- Emphasize data privacy, especially for payments.

### **Exemplar:**
- Member profiles via internal/external accounts.
- Payment processing.
- PCI-DSS compliance.

### **Assessment:**
Your objectives align well with the exemplar's intent. You emphasized **user experience, secure login, and financial compliance**, which match the exemplar’s focus on **account management and PCI-DSS**. You could slightly improve by explicitly referencing **industry standards** like **PCI-DSS** to demonstrate awareness of regulatory requirements.

> **Recommendation:** Add reference to PCI-DSS compliance or similar frameworks to emphasize regulatory alignment.


## ✅ **Stage II – Define the Technical Scope**

### **Your Response:**
- Prioritized **SQL** due to the risk of injection and its central role in data handling.

### **Exemplar:**
- Prioritized **API** due to its attack surface and data exposure.

### **Assessment:**
Both models correctly identify high-risk technologies, but take different focus areas. The exemplar calls attention to **APIs** for external exposure, while yours focuses on **SQL**, which is central to backend integrity.

> **Recommendation:** Acknowledge the **interconnected risks** between SQL and APIs to give a fuller view of the system's attack surface.

## ✅ **Stage III – Decompose the Application**

### **Your Response:**
Described how user searches pass through the **product search process** to the **database**, referencing the diagram and emphasizing **AES, SHA-256, and secure API communication**.

### **Exemplar:**
Indicates user interactions through **frontend, backend, API, and DB**, and highlights need for visual traceability of queries.

### **Assessment:**
Your decomposition effectively captures the app’s structure and process flow. The mention of encryption and API communications shows understanding of technical safeguards.

> **Recommendation:** Incorporate **specific component interactions** (e.g., frontend → API → SQL) for clarity on architecture.


## ✅ **Stage IV – Threat Analysis**

### **Your Response:**
- **Insider misuse**
- **Session hijacking**

### **Exemplar:**
- **Injection**
- **Session hijacking**

### **Assessment:**
You identified **session hijacking**, which is shared with the exemplar, and offered a valid internal threat. While “injection” is a more common and expected external threat, you could explicitly mention it to align closer to common OWASP threats.

> **Recommendation:** Include **SQL injection** as a classic external threat to reinforce known risk vectors.


## ✅ **Stage V – Vulnerability Analysis**

### **Your Response:**
- Lack of prepared statements
- Weak login credentials

### **Exemplar:**
- Lack of prepared statements
- Broken API token

### **Assessment:**
Both models identify **input validation issues** and **authentication gaps**. Your answer reflects a realistic and common vulnerability set. "Weak credentials" is a good addition, though “broken token” may highlight more API-specific issues.

> **Recommendation:** Mention potential **token or session mismanagement** for broader API threat coverage.


## ✅ **Stage VI – Attack Modeling**

### **Your Response:**
Used attack tree showing paths via **SQL injection and session hijacking**, with their exploit mechanisms clearly mapped (e.g., weak credentials, unprepared statements).

### **Exemplar:**
Similar attack tree logic (not shown), connected to MITRE/CVE recommendations.

### **Assessment:**
Your use of the tree is appropriate and structured logically. The representation clearly reflects how vulnerabilities lead to compromises.

> **Recommendation:** Consider referencing **MITRE ATT&CK tactics** or **CVE examples** to elevate credibility and technical depth.


## ✅ **Stage VII – Risk Analysis and Impact**

### **Your Response:**
- Prepared statements
- MFA
- Secure sessions (HTTPS, cookies)
- Code review & pen testing

### **Exemplar:**
- SHA-256
- Incident response
- Password policy
- Least privilege

### **Assessment:**
Your risk controls are **well-aligned and practical**, focusing on proactive and preventative defenses. Compared to the exemplar, you emphasize **prevention and detection**, while the exemplar includes **response and governance controls**.

> **Recommendation:** Include **incident response plans** and **least privilege principles** for a well-rounded risk strategy.


## 🔍 **Final Evaluation**

| **PASTA Stage**                  | **Meets Expectations** | **Comments**                                                                 |
|----------------------------------|-------------------------|------------------------------------------------------------------------------|
| I. Business & Security Objectives | ✅                      | Add explicit regulatory mention (e.g., PCI-DSS).                            |
| II. Technical Scope               | ✅                      | Strong justification; could mention API risk too.                           |
| III. Decompose Application        | ✅                      | Clear; could benefit from detailed component mapping.                       |
| IV. Threat Analysis               | ✅                      | Solid, though add common external threat like injection.                    |
| V. Vulnerability Analysis         | ✅                      | Thorough and aligned with OWASP.                                            |
| VI. Attack Modeling               | ✅                      | Matches tree logic; could benefit from external threat references.          |
| VII. Risk Analysis & Impact       | ✅                      | Excellent coverage; add governance controls (IR, least privilege).          |


### ✅ **Overall Grade: Exceeds Expectations**

You demonstrated a comprehensive and technically accurate application of the PASTA framework. With a few refinements—like adding regulatory references, threat modeling frameworks, and governance-oriented controls—you’re operating at a near-professional level for threat modeling exercises.
