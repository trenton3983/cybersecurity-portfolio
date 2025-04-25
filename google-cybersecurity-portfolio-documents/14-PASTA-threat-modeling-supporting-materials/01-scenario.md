# **PASTA Threat Modeling Activity**

## **Activity Overview**

In this activity, you will practice using the Process of Attack Simulation and Threat Analysis (PASTA) threat model framework. Your objective is to determine whether a new shopping app is safe to launch.  
Threat modeling is an important part of secure software development. Security teams typically perform threat models to identify vulnerabilities before malicious actors do. PASTA is a commonly used framework for assessing the risk profile of new applications.

---

## **Scenario**

You are part of the growing security team at a company for sneaker enthusiasts and collectors. The business is preparing to launch a mobile app that allows customers to buy and sell shoes.  
You will conduct a threat model of the application using the PASTA framework, working through all seven stages to identify security requirements for the app.

---

## **Step-by-Step Instructions**

### **Part 1 – Access the Resources**

**Step 1: Access the template.**

**PASTA Worksheet**

| Stages | Sneaker company |
|--------|------------------|
| I. Define business and security objectives | Make 2-3 notes of specific business requirements that will be analyzed. <br> ● Will the app process transactions? <br> ● Does it do a lot of back-end processing? <br> ● Are there industry regulations that need to be considered? |
| II. Define the technical scope | List of technologies used by the application: <br> ● API <br> ● PKI <br> ● AES <br> ● SHA-256 <br> ● SQL <br><br> Write 2-3 sentences (40-60 words) that describe why you choose to prioritize that technology over the others. |
| III. Decompose application | Sample data flow diagram |
| IV. Threat analysis | List 2 types of threats in the PASTA worksheet that are risks to the information being handled by the application. <br> ● What are the internal threats? <br> ● What are the external threats? |
| V. Vulnerability analysis | List 2 vulnerabilities in the PASTA worksheet that could be exploited. <br> ● Could there be things wrong with the codebase? <br> ● Could there be weaknesses in the database? <br> ● Could there be flaws in the network? |
| VI. Attack modeling | Sample attack tree diagram |
| VII. Risk analysis and impact | List 4 security controls that you’ve learned about that can reduce risk. |

**Step 2: Access supporting materials.**

[Data flow diagram]()

[Sample attack tree]()

---

### **Part 2 – Complete the PASTA Stages**

---

#### **Stage I – Identify the Mobile App’s Business Objectives**

The goal of Stage I is to understand why the app was developed and what it is expected to do.  
**Description from the sneaker company:**
- The app should connect sellers and shoppers seamlessly.
- It should support easy sign-up, login, and account management.
- Data privacy is a major concern.
- Buyers can message sellers and rate them to encourage good service.
- Sales should be fast and clear, with multiple payment options.
- Proper payment handling is crucial to avoid legal issues.

**Instructions:**  
In the Stage I row of the PASTA worksheet, list 2-3 business objectives based on the description above.

---

#### **Stage II – Evaluate the App’s Components**

In this stage, the technological scope is defined.

**Technologies used by the app include:**
- API: Used for component interaction and adding functionality via third-party services.
- PKI (AES & RSA): AES encrypts sensitive data (e.g., credit card info), RSA is used for key exchanges.
- SHA-256: Protects sensitive data like passwords.
- SQL: Stores and accesses data related to sneakers and sellers.

**Instructions:**  
Choose one of the technologies above to evaluate first.  
In the Stage II row, write 2-3 sentences (40–60 words) explaining why you prioritize it and the risks it presents.

---

#### **Stage III – Review a Data Flow Diagram**

This stage focuses on how the application handles information.  
**Example process:** Buyers search the database for shoes.

**Instructions:**  
Open and review the PASTA data flow diagram resource. Consider how previously evaluated technologies help protect user data in this process.

---

#### **Stage IV – Use an Attacker Mindset to Analyze Potential Threats**

Here, you identify threats to both the technologies (from Stage II) and the processes (from Stage III).  
**Example:** Authentication could be attacked via malware or social engineering.

**Instructions:**  
In the Stage IV row, list 2 types of threats relevant to the sneaker app’s information handling.  
**Pro Tip:** Internal system logs are great for gathering threat intelligence.

---

#### **Stage V – List Vulnerabilities Exploitable by Threats**

This is the vulnerability analysis phase. Consider the attack surface of technologies from Stage II.  
**Example:** A payment form might be vulnerable if it doesn't encrypt data properly.

**Instructions:**  
In Stage V of the worksheet, list 2 vulnerabilities that could be exploited by threat actors.  
**Pro Tip:** Use CVE® and OWASP for examples of common vulnerabilities.

---

#### **Stage VI – Map Assets, Threats, and Vulnerabilities to an Attack Tree**

This stage uses previous information to construct an attack tree.

**Instructions:**  
Open and review the PASTA attack tree resource. Use it to understand how threat actors exploit app vulnerabilities.

---

#### **Stage VII – Identify New Security Controls to Reduce Risk**

The final stage focuses on implementing security defenses.

**Instructions:**  
In the Stage VII row, list 4 security controls that can reduce the risk of data breaches or similar incidents.

---

## **What to Include in Your Response**

Your completed activity should include:
- ✅ 2–3 business objectives  
- ✅ 2–3 technology requirements  
- ✅ 2 potential threats  
- ✅ 2 system vulnerabilities  
- ✅ 4 defenses that limit risk
