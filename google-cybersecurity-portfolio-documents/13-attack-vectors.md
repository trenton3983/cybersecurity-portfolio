# Scenario

## USB Baiting: Risk Assessment Activity  
**Rhetorical Hospital Cybersecurity Scenario**

In this activity, you will assess the **attack vectors** of a USB drive. You will explore a USB baiting scenario from both the **attacker** and **target** perspectives.

USB flash drives are commonly used for data storage and transfer, but their convenience introduces security risks. Threat actors can exploit USBs to:

- Deliver malicious software  
- Damage hardware  
- Take control of devices or networks  

**USB baiting** is a social engineering attack in which a malicious USB is deliberately left for someone to find. Once inserted, the device can infect the host system or provide access to sensitive information.

---

### Hospital Parking Lot Discovery

You are on the security team at Rhetorical Hospital. One morning, you find a USB stick with the hospital’s logo in the parking lot. No one else is nearby, so you pick it up out of curiosity.

Back in your office, you plug the USB drive into a **virtualized workstation**. Virtualization allows secure inspection of untrusted devices because the simulated environment is isolated from production systems.

The USB appears to belong to **Jorge Bailey**, the hospital's HR manager. The drive contains:

![Drive Contents](assets/images/usb-drive.png)

---

## Completed Activity

### Parking Lot USB Exercise

#### Contents  
The USB contains both **personal and professional** files. Personal content includes folders like _"Family photos"_, _"Our dog pics 🐶"_, a **wedding list**, and a **vacation ideas** document. Work-related files include a **new hire letter**, **employee budget spreadsheet**, **shift schedules**, and a **resume** labeled _"JB_Resume."_ This mix of **personally identifiable information (PII)** and **organizational documents** significantly increases the risk of data leakage and potential exploitation.

#### Attacker Mindset  
An attacker could use these files to craft convincing **spear-phishing emails** using Jorge’s identity or HR position. The wedding list and vacation plans offer personal context for manipulating Jorge or his contacts. Access to shift schedules, budget data, or HR documents could be used to impersonate internal staff or plan attacks on hospital infrastructure. The hospital-branded USB adds further credibility, increasing the risk of **trust-based exploitation**.

#### Risk Analysis  
USB baiting attacks can be used to deploy **malware** such as keyloggers, ransomware, or data exfiltration tools. If an employee had accessed this USB outside of a sandbox, the entire network could be compromised. Files like the resume and employee schedule provide enough information for a threat actor to launch **social engineering attacks** or **map the organization’s structure**.

To mitigate these risks, organizations should implement:

- **Technical controls**: Disable auto-run for USBs, use USB control software, and scan all external devices.  
- **Operational policies**: Mandate USB inspection within virtual machines and isolate unknown devices.  
- **Managerial actions**: Educate staff about baiting tactics and enforce a clear policy for handling found devices.  

---

## Exemplar

**Contents**: The contents of the USB drive contain files that appear to belong to a specific person. It contains a mixture of personal and business-related information that should not be stored in the same place.  

**Attacker mindset**: Any information that an attacker obtains can be used against someone. Information on a USB drive should be encrypted regardless of whether it’s personal or work-related.  

**Risk analysis**: It’s unsafe to plug an unfamiliar USB drive into your computer because of the wide range of attacks that can be hidden on them. Promoting employee awareness of USB baiting attacks is a managerial control that can reduce the risks of a negative event. Routinely scanning for viruses is an example of an operational control that can be implemented. Disabling Autoplay on all PCs is a technical precaution that can be taken.

---

# ChatGPT Comparison Assessment

## ✅ Contents

### Exemplar Summary
- Identifies personal and work files  
- Highlights PII exposure and hospital operations  
- Notes the risk of combining personal and professional content  

### Completed Version  
> “The USB contains both personal and professional files... wedding list, vacation ideas... new hire letter, employee budget spreadsheet, shift schedules, and a resume... This mix of personally identifiable information (PII) and organizational documents significantly increases the risk of data leakage and potential exploitation.”

### Assessment
- ✅ **Strengths**: Clearly identifies the nature and diversity of files; recognizes both PII and operational data risks; meets the 2–3 sentence requirement  
- 🔍 **Possible Improvement**: Could explicitly state that these files should not be stored together or highlight how the presence of work-related files creates organizational exposure  

---

## ✅ Attacker Mindset

### Exemplar Summary
- Notes the attacker could use data for deception (phishing)  
- Shows how personal/work information enables manipulation  
- Example: Email spoofing a coworker or relative  

### Completed Version  
> “An attacker could use these files to craft convincing spear-phishing emails... The wedding list and vacation plans offer personal context... Access to shift schedules, budget data, or HR documents...”

### Assessment
- ✅ **Strengths**: Incorporates spear-phishing, social engineering, and identity impersonation. It offers concrete examples of how an attacker could use both types of data  
- 🔍 **Possible Improvement**: Could have tied back more explicitly to Jorge (e.g., “targeting Jorge using his known contacts”) for alignment with the exemplar’s personal focus  

---

## ✅ Risk Analysis

### Exemplar Summary
- Breaks down technical (disable AutoPlay), operational (AV scans), and managerial (training) controls  
- Notes that attacks can be hidden even in files that appear harmless  

### Completed Version  
> “USB baiting attacks can be used to deploy malware such as keyloggers... compromised the hospital’s network...  
To mitigate these risks, organizations should implement:  
> - Technical controls...  
> - Operational policies...  
> - Managerial actions...”

### Assessment
- ✅ **Strengths**: Thorough and well-structured; uses the same three control categories as the exemplar; lists specific examples like USB control software, sandbox inspection, and staff education  
- 🔍 **Possible Improvement**: Could briefly reinforce that risk remains even if no malware is detected, as the exemplar does  

---

## 🔎 Overall Assessment Summary

| Criteria         | Score | Notes                                                                 |
|------------------|-------|------------------------------------------------------------------------|
| **Contents**      | ✅     | Meets all criteria; a bit more emphasis on mixing file types could help |
| **Attacker Mindset** | ✅     | Effectively explains attack paths; could strengthen personalization      |
| **Risk Analysis**  | ✅     | Excellent structure and depth; mirrors the exemplar’s categories well    |

---

## 🌟 Final Verdict: Well Done

Your response meets or exceeds the exemplar's expectations. It includes more specific examples, demonstrates strong **threat modeling**, and clearly distinguishes between **technical**, **operational**, and **managerial** mitigation strategies. Only minor tweaks could make it even tighter for alignment with the exemplar's style.
