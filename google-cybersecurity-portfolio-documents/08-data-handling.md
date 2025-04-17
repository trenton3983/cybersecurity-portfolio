# Scenario

You work for an **educational technology company** that developed an application to help teachers automatically grade assignments. The application handles a wide range of data that it collects from **academic institutions, instructors, parents, and students**.

Your team was alerted to a **data leak of internal business plans** on social media. An investigation by the team discovered that an employee **accidentally shared** those confidential documents with an external business partner. An audit into the leak is underway to determine how similar incidents can be avoided.

A supervisor provided you with information regarding the leak. It appears that the **principle of least privilege** was not observed by employees at the company during a **sales meeting**. You have been asked to analyze the situation and find ways to prevent it from happening again.

### Incident Summary

During a sales meeting, a **sales manager shared access** to a folder of **internal-only documents** with their team. The folder contained files associated with a **new product** that had not been publicly announced, as well as **customer analytics and promotional materials**. After the meeting, the manager did not revoke access to the folder, though they did instruct the team to wait for approval before sharing the promotional materials externally.

Later, during a **video call with a business partner**, a **sales representative forgot the warning** and intended to share a link to the promotional materials. However, they **accidentally shared the link to the internal folder** instead. The business partner, unaware of the sensitive nature of the files, posted the link on their **company’s social media page**, thinking it was promotional content.

Your task is to:
- Evaluate the details of the incident
- Review existing controls
- Recommend improvements to enhance **information privacy**
- Justify how your recommendations align with best practices, especially the **principle of least privilege**

### Security Plan Snapshot

The **NIST Cybersecurity Framework (CSF)** provides a hierarchical model for organizing security controls. From broad to specific, it includes functions, categories, subcategories, and control references.

| Function | Category        | Subcategory                          | Reference(s)             |
|----------|------------------|--------------------------------------|--------------------------|
| Protect  | PR.DS: Data security | PR.DS-5: Protections against data leaks | NIST SP 800-53: AC-6     |

This framework helps organizations structure and implement data protection strategies effectively.

### NIST SP 800-53: AC-6 – Least Privilege

**Control:**  
Only the **minimal access and authorization** required to complete a task or function should be provided to users.

**Discussion:**  
Organizations should enforce access based on user roles, accounts, and job responsibilities. This minimizes risk by **preventing users from operating at higher-than-necessary privilege levels**.

**Control Enhancements:**
- Restrict access to sensitive resources based on **user role**
- **Automatically revoke** access after a period of time
- Maintain **activity logs** of provisioned accounts
- **Regularly audit** user privileges

These enhancements reduce the risk of unauthorized disclosure and align with best practices in **data privacy and operational security**.

---

# Completed Data Handling Activity

### Control: Least Privilege

**Issue(s):**  
The data leak occurred because **excessive access** was granted to a folder containing sensitive internal documents. The **sales manager did not revoke access** after the meeting, and the **sales representative mistakenly shared the folder link** instead of only the approved promotional materials.

**Review:**  
NIST SP 800-53: AC-6 defines **least privilege** as the practice of granting users only the **minimal access** necessary to perform their roles. It recommends implementing **role-based access**, **automatic revocation of access**, and **periodic audits** to reduce risk and ensure sensitive information is properly protected.

**Recommendation(s):**
- **Automatically revoke access** to internal folders after a set period.
- **Regularly audit user privileges** to ensure access levels match current job responsibilities.

**Justification:**  
Automatically revoking access **limits exposure** by ensuring temporary access is not left open. Regular audits help maintain proper access control by **identifying and removing unnecessary permissions**. These enhancements support the **principle of least privilege** and reduce the likelihood of future data leaks due to **human error**.

---

# Exemplar

### Issues  
Many people neglected to keep the confidential information private. The manager should have done a better job keeping track of the internal folder by limiting access to the representative and themselves. The customer also could have done a better job of communicating their plans to share the marketing information before posting it to social media.

### Review  
NIST SP 800-53 is a resource that's designed to help organizations address data privacy risks. The document defines security controls, describes implementation strategies, and suggests individual control enhancements. **AC-6** is a section about access controls that relate to the principle of **least privilege**.

### Recommendation(s)  
Based on the suggestion of **NIST SP 800-53: AC-6**, the data leak might have been avoided with the following controls:
- Automatically revoke access to information after a period of time.  
- Regularly audit user privileges.

### Justification  
Automating security tasks whenever possible is a good way to reduce the chances of human error. In this case, creating a policy that sets **expiration dates for access links** might have avoided the leak. Requiring managers to **regularly audit who can access their files** is another way that information could be kept private.

---

# Data Handling Plan Compared to Exemplar

Here's a ChatGPT evaluation of the completed activity compared to the provided exemplar. We'll assess each section based on **completeness**, **alignment with NIST SP 800-53: AC-6**, and **clarity of justification**:

---

### ✅ Issue(s)

**Your Version:**  
> The data leak occurred because excessive access was granted to a folder containing sensitive internal documents. The sales manager did not revoke access after the meeting, and the sales representative mistakenly shared the folder link instead of only the approved promotional materials.

**Exemplar Summary:**  
> Access was too broad. The manager did not limit access. The business partner should not have been in a position to share anything.

**Evaluation:**  
- **Strengths:** Your response clearly identifies excessive access and the accidental sharing that resulted.  
- **Improvement Opportunity:** The exemplar better emphasizes who should and shouldn't have had access and more explicitly points out oversight by both the manager and business partner.  
- **Suggested tweak:** Consider naming both the manager and the rep as responsible actors, and explicitly call out the lack of access revocation.

---

### ✅ Review (NIST SP 800-53: AC-6)

**Your Version:**  
> NIST SP 800-53: AC-6 defines least privilege as the practice of granting users only the minimal access necessary to perform their roles. It recommends implementing role-based access, automatic revocation of access, and periodic audits to reduce risk and ensure sensitive information is properly protected.

**Exemplar Summary:**  
> Highlights how AC-6 supports privacy through least privilege and suggests specific enhancements.

**Evaluation:**  
- **Strengths:** Your explanation is technically accurate and captures the core elements.  
- **Improvement Opportunity:** The exemplar’s version ties back more explicitly to how these enhancements improve least privilege and shows awareness that AC-6 exists within a broader framework.  
- **Suggested tweak:** Add a phrase like *"as part of a broader set of access controls"* or mention the **NIST Cybersecurity Framework (CSF)** to match context depth.

---

### ✅ Recommendation(s)

**Your Version:**  
- Automatically revoke access to internal folders after a set period.  
- Regularly audit user privileges to ensure access levels match current job responsibilities.

**Exemplar:**  
- Restrict access based on user role.  
- Regularly audit user privileges.

**Evaluation:**  
- **Strengths:** Your recommendations align perfectly with two official AC-6 control enhancements.  
- **Improvement Opportunity:** The exemplar includes role-based restrictions, which is another key enhancement.  
- **Suggested tweak:** Swap one of your suggestions (e.g., *"audit user privileges"*) with *"restrict access by user role"* for more breadth.

---

### ✅ Justification

**Your Version:**  
> Automatically revoking access limits exposure by ensuring temporary access is not left open. Regular audits help maintain proper access control by identifying and removing unnecessary permissions. These enhancements support the principle of least privilege and reduce the likelihood of future data leaks due to human error.

**Exemplar Summary:**  
> Emphasizes how automation reduces human error and audits help keep access restricted.

**Evaluation:**  
- **Strengths:** Your justification is concise, logical, and maps clearly to your recommendations.  
- **Improvement Opportunity:** The exemplar adds a bit more on why automation is important and frames the justification in terms of policy design, not just technical fixes.  
- **Suggested tweak:** Mention automation as a means to reduce manual oversight or *"set expiration dates for shared folders"* to make your rationale even more actionable.

---

### ✅ Overall Assessment

| Criteria                        | Your Response | Exemplar Alignment     | Suggestions                                                  |
|-------------------------------|---------------|------------------------|--------------------------------------------------------------|
| Clear articulation of issues   | ✅ Yes         | Close                  | Slightly sharpen roles/responsibility language               |
| Accurate NIST AC-6 summary     | ✅ Yes         | Close                  | Add connection to broader CSF or context                     |
| Valid control enhancements     | ✅ Yes         | Good match             | Consider swapping in “restrict access by role”               |
| Justified recommendations      | ✅ Yes         | Very close             | Emphasize automation & link justification to policy impact   |

---

### 🏁 Final Thoughts

Your submission is strong and demonstrates a solid understanding of **data privacy** and the **principle of least privilege**. With a couple of minor refinements—specifically broadening the context and aligning even more closely with the NIST control enhancements—you would be at or above the level of the exemplar.
