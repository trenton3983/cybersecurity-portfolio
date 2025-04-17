# Controls and Compliance Checklist Exemplar

## Controls Assessment Checklist

> Type an X in the “yes” or “no” column to answer the question:  
> Does Botium Toys currently have this control in place?

| Yes | No  | Control                                     | Explanation |
|-----|-----|---------------------------------------------|-------------|
|     |  X  | Least Privilege                             | Currently, all employees have access to customer data; privileges need to be limited to reduce the risk of a breach. |
|     |  X  | Disaster recovery plans                      | There are no disaster recovery plans in place. These need to be implemented to ensure business continuity. |
|     |  X  | Password policies                            | Employee password requirements are minimal, which could allow a threat actor to more easily access secure data/other assets via employee work equipment/the internal network. |
|     |  X  | Separation of duties                         | Needs to be implemented to reduce the possibility of fraud/access to critical data, since the company CEO currently runs day-to-day operations and manages the payroll. |
|  X  |     | Firewall                                     | The existing firewall blocks traffic based on an appropriately defined set of security rules. |
|     |  X  | Intrusion detection system (IDS)             | The IT department needs an IDS in place to help identify possible intrusions by threat actors. |
|     |  X  | Backups                                      | The IT department needs to have backups of critical data, in the case of a breach, to ensure business continuity. |
|  X  |     | Antivirus software                           | Antivirus software is installed and monitored regularly by the IT department. |
|     |  X  | Manual monitoring, maintenance, and intervention for legacy systems | Legacy systems are monitored and maintained, but not on a regular schedule and without clear intervention policies, placing systems at risk. |
|     |  X  | Encryption                                   | Encryption is not currently used; implementing it would provide greater confidentiality of sensitive information. |
|     |  X  | Password management system                   | There is no password management system currently in place; implementing this control would improve productivity in the case of password issues. |
|  X  |     | Locks (offices, storefront, warehouse)       | The store’s physical location has sufficient locks. |
|  X  |     | Closed-circuit television (CCTV) surveillance| CCTV is installed/functioning at the store’s physical location. |
|  X  |     | Fire detection/prevention                    | Botium Toys has a functioning fire detection and prevention system. |


## Compliance Checklist

> Type an X in the “yes” or “no” column to answer the question:  
> Does Botium Toys currently adhere to this compliance best practice?

### Payment Card Industry Data Security Standard (PCI DSS)

| Yes | No  | Best Practice | Explanation |
|-----|-----|---------------|-------------|
|     |  X  | Only authorized users have access to customers’ credit card information | All employees currently have access to the company’s internal data. |
|     |  X  | Credit card information is securely stored/processed | Credit card information is not encrypted and all employees currently have access to it. |
|     |  X  | Implement data encryption procedures | The company does not currently use encryption to protect customers’ financial information. |
|     |  X  | Adopt secure password management policies | Password policies are nominal and no password management system is in place. |

### General Data Protection Regulation (GDPR)

| Yes | No  | Best Practice | Explanation |
|-----|-----|---------------|-------------|
|     |  X  | E.U. customers’ data is secured | The company does not use encryption to ensure confidentiality of customer information. |
|  X  |     | Notification plan within 72 hours of breach | A plan exists to notify E.U. customers within 72 hours of a data breach. |
|     |  X  | Data properly classified and inventoried | Assets are listed but not classified. |
|  X  |     | Enforce privacy policies and procedures | Privacy policies and procedures have been developed and enforced among IT and staff. |

### System and Organization Controls (SOC 1 & SOC 2)

| Yes | No  | Best Practice | Explanation |
|-----|-----|---------------|-------------|
|     |  X  | User access policies are established | Controls of Least Privilege and separation of duties are not in place. |
|     |  X  | Sensitive data (PII/SPII) is confidential | Encryption is not in place to ensure confidentiality. |
|  X  |     | Data integrity is ensured | Data is consistent, complete, accurate, and validated. |
|  X  |     | Data available to authorized users | Data is available to all employees; access must be limited to job-required users only. |


## Recommendations

Multiple controls need to be implemented to improve Botium Toys’ security posture and ensure the confidentiality of sensitive information, including:

- Least Privilege  
- Disaster recovery plans  
- Password policies  
- Separation of duties  
- Intrusion detection system (IDS)  
- Ongoing legacy system management  
- Encryption  
- Password management system  

To address compliance gaps, Botium Toys must implement Least Privilege, separation of duties, and encryption. Asset classification is also necessary to identify further required controls.
