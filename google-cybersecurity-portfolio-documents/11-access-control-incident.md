# Access Control Assessment Activity

In this activity, you will assess the access controls used by a business. You will analyze their current process, identify issues, and make recommendations to improve their security practices.

Previously, you learned that access controls are security controls that manage access, authorization, and accountability of information. Authentication controls are used to verify identity, whereas authorization controls determine what a user is permitted to do. When implemented effectively, access controls significantly reduce the likelihood of a security risk.

---

## Scenario

You are the first cybersecurity professional hired by a growing business.

Recently, a payment was initiated from the company to an unknown bank account. The finance manager insists that no error was made on their part. Fortunately, the payment was intercepted and stopped in time. The business owner has tasked you with investigating the incident and identifying how it happened to prevent future occurrences.

Your objective is to perform an incident analysis and evaluate the current access control mechanisms in use. This includes identifying the source of the incident, analyzing user permissions, detecting weaknesses in authentication and authorization, and providing recommendations to mitigate future risks.

To begin, you will examine the event log tied to the incident. Next, you will review the employee directory to trace system access and assess user privileges. Finally, you will document your findings and suggest improvements to the company’s access control policies.

---

## Event Log

| Field            | Value                        |
|------------------|------------------------------|
| **Event Type**   | Information                  |
| **Event Source** | AdsmEmployeeService          |
| **Event ID**     | 1227                         |
| **Date**         | 10/03/2023                   |
| **Time**         | 8:29:57 AM                   |
| **User**         | Legal\Administrator          |
| **Computer**     | Up2-NoGud                    |
| **IP Address**   | 152.207.255.255              |
| **Description**  | Payroll event added. FAUX_BANK |

---

## Employee Directory

| Name              | Role               | Email                      | IP Address         | Status      | Authorization | Last Access         | Start Date | End Date     |
|-------------------|--------------------|-----------------------------|---------------------|-------------|----------------|----------------------|------------|--------------|
| Lisa Lawrence     | Office manager     | l.lawrence@erems.net       | 118.119.20.150      | Full-time   | Admin          | 12:27:19 pm (0 min)  | 2019-10-01 | N/A          |
| Jesse Pena        | Graphic designer   | j.pena@erems.net           | 186.125.232.66      | Part-time   | Admin          | 4:55:05 pm (1 day)   | 2020-11-16 | N/A          |
| Catherine Martin  | Sales associate    | catherine_M@erems.net      | 247.168.184.57      | Full-time   | Admin          | 12:17:34 am (10 min) | 2019-10-01 | N/A          |
| Jyoti Patil       | Account manager    | j.patil@erems.net          | 159.250.146.63      | Full-time   | Admin          | 10:03:08 am (2 hrs)  | 2019-10-01 | N/A          |
| Joanne Phelps     | Sales associate    | j_phelps123@erems.net      | 249.57.94.27        | Seasonal    | Admin          | 1:24:57 pm (2 yrs)   | 2020-11-16 | 2020-01-31   |
| Ariel Olson       | Owner              | a.olson@erems.net          | 19.7.235.151        | Full-time   | Admin          | 12:24:41 pm (4 min)  | 2019-08-01 | N/A          |
| **Robert Taylor Jr.** | **Legal attorney** | **rt.jr@erems.net**     | **152.207.255.255** | Contractor  | Admin          | **8:29:57 am (5 days)** | 2019-09-04 | **2019-12-27** |
| Amanda Pearson    | Manufacturer       | amandap987@erems.net       | 101.225.113.171     | Contractor  | Admin          | 6:24:19 pm (3 mo)    | 2019-08-05 | N/A          |
| George Harris     | Security analyst   | georgeharris@erems.net     | 70.188.129.105      | Full-time   | Admin          | 05:05:22 pm (1 day)  | 2022-01-24 | N/A          |
| Lei Chu           | Marketing          | lei.chu@erems.net          | 53.49.27.117        | Part-time   | Admin          | 3:05:00 pm (2 days)  | 2020-11-16 | 2020-01-31   |

---

## Step-By-Step Instructions

Use the following table to complete your investigation and recommendations.

| Note(s) | Issue(s) | Recommendation(s) |
|---------|----------|-------------------|
| **Authorization / Authentication** | **Objective:** Make 1-2 notes of information that can help identify the threat: <br> - Who caused this incident? <br> - When did it occur? <br> - What device was used? | **Objective:** Based on your notes, list 1-2 authorization issues: <br> - What level of access did the user have? <br> - Should their account be active? | **Objective:** Make at least 1 recommendation that could prevent this kind of incident: <br> - Which technical, operational, or managerial controls could help? |

Once you have filled out your notes, issues, and recommendations, proceed to the next course item to compare your work with a completed exemplar.

---

# Access Control Assessment: Incident Review

## Notes (User Identification)
- The incident occurred on **10/03/2023 at 8:29:57 AM** from IP address **152.207.255.255**.
- The user account used was **"Legal\Administrator"**, and the device was named **Up2-NoGud**.
- This IP and username correspond to **Robert Taylor Jr.**, a contractor whose end date was **2019-12-27** but still retained **Admin** access.

## Issues (Access Control Flaws)
- **Inactive or terminated personnel** still have **active accounts with administrative privileges**.
- There is **no access deprovisioning policy**, which allows former employees to access sensitive systems long after their contracts end.

## Recommendations (Access Control Mitigations)
- Establish an **automated offboarding workflow** that revokes all access (accounts, devices, credentials) when an employee or contractor leaves the organization.
- Enforce a **least privilege policy**, ensuring that only essential personnel hold admin rights, and require **periodic audits** of user accounts to validate status and necessity.

---

# ✅ Exemplar: Access Control Assessment

## Note(s) about the User
- The event took place on **10/03/23**.
- The user is **Legal/Administrator**.
- The IP address of the computer used to log in is **152.207.255.255**.

> *Event logs can often help you identify the who, what, and why of a security incident.*

## Access Control Issue(s)
- **Robert Taylor Jr.** is a contractor with admin access.
- His contract ended in **2019**, but his account accessed payroll systems in **2023**.
- Oftentimes, incidents like this occur because systems are **misconfigured or misused**. That is the case with how this business is **sharing information among its employees**.

## Recommendations
- **User accounts should expire after 30 days**.
- **Contractors should have limited access** to business resources.
- **Enable multi-factor authentication (MFA)**.

> It appears as though a former employee is potentially the threat actor. However, it's possible that they were not the person responsible for this security incident.

---

# ✅ ChatGPT Comparison: Your Response vs. Completed Exemplar

## 1. Notes (User Identification)

**Exemplar includes:**
- Date of incident: 10/03/23  
- Username: Legal/Administrator  
- IP address: 152.207.255.255  

**Your submission includes:**
- All of the above plus additional context:
  - Device name: **Up2-NoGud**
  - Identified matching user: **Robert Taylor Jr.**
  - Employment status: **Contractor, end date 2019-12-27**

**Assessment:**
- ✅ **Strength:** You go beyond the exemplar by mapping log details directly to the employee directory and identifying the user by name and status, demonstrating deeper analysis.
- 🔧 **Improvement:** None necessary; your level of detail is strong and exceeds expectations.

---

## 2. Issues (Access Control Flaws)

**Exemplar notes:**
- Former contractor still has admin access post-contract.
- Indicates misuse or misconfiguration of access systems.

**Your submission states:**
- Terminated contractor still has admin access.
- No deprovisioning or access audit policy.

**Assessment:**
- ✅ **Strength:** You clearly define the lack of access deprovisioning and highlight policy-level failures.
- 🔧 **Improvement:** The exemplar points out that contractors should have limited access, which adds an operational control perspective. You could add this point to strengthen the systemic risk analysis.

---

## 3. Recommendations (Mitigations)

**Exemplar includes:**
- User accounts should expire after 30 days.
- Limit contractor access.
- Enable multi-factor authentication (MFA).

**Your submission includes:**
- Implement an **automated offboarding process**.
- Enforce **least privilege access** and conduct regular **access audits**.

**Assessment:**
- ✅ **Strength:** Your recommendations are operationally sound, cover both technical and managerial controls, and support preventative security culture.
- 🔧 **Improvement:** Consider explicitly recommending **MFA** or **expiration timelines**, which align with industry best practices and were highlighted in the exemplar.

---

## 📌 Summary of Strengths
- You conducted a **deeper investigation** by cross-referencing logs with employee data to identify the user by name and employment status.
- Your recommendations are **more process-oriented**, showing maturity in understanding broader organizational controls.
- You identified both **technical and managerial issues** — an important step in real-world risk mitigation.

---

## 🛠️ Areas for Minor Improvement
- Include specific **technical safeguards** like MFA or access expiration rules to directly mitigate credential compromise.
- Mention that **contractors should have more restricted access**, especially when no longer active.

---

## ✅ Final Evaluation
Your submission meets and exceeds the expectations set by the exemplar in several areas, particularly in **depth of investigation** and the **completeness of your reasoning**. With a few added technical recommendations (like MFA), your assessment would align perfectly with best practices in access control security.
