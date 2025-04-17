# Botium Toys Security Audit

## Step 1: Review Supporting Materials

### Audit Scope and Goals

**Scope:**  
Entire security program at Botium Toys, including assets, internal processes, and procedures related to security controls and compliance best practices.

**Goals:**  
- Assess existing assets  
- Complete controls and compliance checklist  
- Identify areas to improve security posture

### Current Assets Managed by IT Department

- On-premises office equipment  
- Employee devices (desktops, laptops, smartphones, etc.)  
- Storefront and warehouse products  
- Systems and software (accounting, telecommunication, database, security, ecommerce, inventory management)  
- Internet access and internal network  
- Data retention/storage systems  
- Legacy system maintenance

### Risk Assessment

**Overall Risk Score:** 8 (High)

**Key Concerns:**
- Inadequate asset management and controls  
- Potential fines due to non-compliance  
- Employees have unrestricted access to customer PII/SPII and credit card data  
- No encryption in use for credit card data  
- Lack of proper access controls (least privilege/separation of duties)  
- No disaster recovery plans or data backups  
- Password policies do not meet minimum complexity requirements  
- Absence of centralized password management  
- Legacy systems are irregularly maintained

**Existing Strengths:**
- Firewall is properly configured  
- Antivirus software is installed and regularly monitored  
- Physical location secured with locks, CCTV, and fire prevention systems  
- EU breach notification policy established



## Step 2: Conduct Audit – Controls and Compliance Checklist

### Controls Checklist

| Control                         | Status |
|---------------------------------|--------|
| Least Privilege                 | ❌ No  |
| Disaster recovery plans         | ❌ No  |
| Password policies               | ❌ No  |
| Separation of duties            | ❌ No  |
| Firewall                        | ✅ Yes |
| Intrusion detection system (IDS)| ❌ No  |
| Backups                         | ❌ No  |
| Antivirus software              | ✅ Yes |
| Manual monitoring of legacy systems | ❌ No (irregular and unclear) |
| Encryption                      | ❌ No  |
| Password management system      | ❌ No  |
| Locks (offices, storefront, warehouse) | ✅ Yes |
| CCTV surveillance               | ✅ Yes |
| Fire detection/prevention systems | ✅ Yes |

### Compliance Checklist

#### **Payment Card Industry Data Security Standard (PCI DSS):**
- Only authorized users access credit card data: ❌ No  
- Credit card data securely stored/processed: ❌ No  
- Data encryption procedures implemented: ❌ No  
- Secure password management policies adopted: ❌ No  

#### **General Data Protection Regulation (GDPR):**
- E.U. customers’ data secured: ❌ No (general data handling weak, though breach notification is in place)  
- Notification plan within 72 hours of breach: ✅ Yes  
- Proper data classification and inventory: ❌ No  
- Privacy policies enforced/documented: ✅ Yes  

#### **System and Organization Controls (SOC 1 & SOC 2):**
- User access policies established: ❌ No  
- Sensitive data confidentiality: ❌ No  
- Data integrity ensured: ✅ Yes  
- Data availability for authorized users: ✅ Yes  



## Recommendations

- Implement a robust disaster recovery plan and regular backups of critical data  
- Immediately enforce encryption for sensitive customer and cardholder data  
- Establish least privilege and separation of duties policies to restrict unauthorized data access  
- Strengthen password policies to meet complexity requirements, and implement a centralized password management system  
- Deploy an intrusion detection system (IDS) to proactively detect security threats  
- Regularly schedule and clearly document maintenance for legacy systems  
- Conduct thorough classification and inventory of all data to comply with GDPR and PCI DSS
