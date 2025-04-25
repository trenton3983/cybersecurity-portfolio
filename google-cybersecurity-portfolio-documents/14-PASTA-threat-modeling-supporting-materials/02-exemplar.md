# Completed Exemplar

## PASTA Worksheet  
**Stages: Sneaker Company**


### I. Define Business and Security Objectives

Make 2-3 notes of specific business requirements that will be analyzed:
- Users can create member profiles internally or by connecting external accounts.  
- The app must process financial transactions.  
- The app should be in compliance with PCI-DSS.  


### II. Define the Technical Scope

List of technologies used by the application:
- Application programming interface (API)  
- Public key infrastructure (PKI)  
- Advanced encryption system (AES)  
- SHA-256  
- SQL  

**Notes:**  
APIs facilitate the exchange of data between customers, partners, and employees, so they should be prioritized. They handle a lot of sensitive data while connecting various users and systems together. However, details such as which APIs are being used should be considered before prioritizing one over another. APIs can be prone to security vulnerabilities due to a larger attack surface.


### III. Decompose Application

**Sample data flow diagram**  
(Note: Diagram not shown in this text format, but this section should include how user requests move through application components such as frontend, backend, API, and database.)

### IV. Threat Analysis

List 2 types of threats that are risks to the information handled by the application:
- Injection  
- Session hijacking  


### V. Vulnerability Analysis

List 2 vulnerabilities that could be exploited:
- Lack of prepared statements  
- Broken API token  


### VI. Attack Modeling

**Sample attack tree diagram**  
(Note: Diagram not shown in this text format, but this should logically connect how an attacker might exploit vulnerabilities to compromise assets.)


### VII. Risk Analysis and Impact

List 4 security controls that can reduce risk:
- SHA-256  
- Incident response procedures  
- Password policy  
- Principle of least privilege  


## Assessment of Exemplar


### Stage I: Define Business and Security Objectives

**Summary:**  
These objectives are defined early by asking broad questions about the application’s purpose. For example: How does the app make money? Understanding this helps guide future steps.

**Recommendations:**  
A shopping application must process payments. Therefore, technologies are needed to ensure data privacy, security, and PCI-DSS compliance.


### Stage II: Define the Technical Scope

**Summary:**  
This stage focuses on identifying technologies used in the application to understand its attack surface and dependencies.

**Recommendations:**  
Since APIs handle significant sensitive data, they need special attention. However, be sure to evaluate specific API implementations when prioritizing defenses.


### Stage III: Decompose the Application

**Summary:**  
Builds on Stage II by analyzing how different components communicate and how security controls are currently applied.

**Recommendations:**  
Check whether the MySQL database uses prepared statements to prevent SQL injection. The data flow diagram should show the path of a typical search or transaction.


### Stage IV: Threat Analysis

**Summary:**  
Focuses on identifying threats based on the technology stack and data types processed by the application.

**Recommendations:**  
- Injection attacks are common in SQL environments.  
- Session hijacking can occur due to cookie misuse across app layers.  
Identify the threats that match your application’s structure and security gaps.


### Stage V: Vulnerability Analysis

**Summary:**  
This stage links design/code issues to the threats already identified.

**Recommendations:**  
- A lack of prepared statements enables SQL injection.  
- Session hijacking becomes likely if cookies are not securely managed.


### Stage VI: Attack Modeling

**Summary:**  
Use attack trees to show how the vulnerabilities and threats identified are practically exploitable.

**Recommendations:**  
Reference frameworks like MITRE ATT&CK or CVE to support your model. Diagrams should show logical attack paths.


### Stage VII: Risk Analysis and Impact

**Summary:**  
This stage focuses on reducing identified risks and planning for those that remain.

**Recommendations:**  
Controls like SHA-256, a defined incident response process, a clear password policy, and enforcing least privilege can significantly reduce risk before product launch.  
