# Incident Report Analysis

[Supporting Documents](/google-cybersecurity-portfolio-documents/03-incidident-report-analysis-supporting-documents)

## Summary
On Friday, March 28, 2025, the organization experienced a Distributed Denial of Service (DDoS) attack that disrupted internal network services for approximately two hours. The incident was caused by an external flood of ICMP packets, which overwhelmed the network infrastructure and made internal systems unresponsive.

The attack exploited an unconfigured firewall, allowing the traffic to pass through unchecked. In response, the incident management team blocked incoming ICMP packets, shut down non-critical services, and prioritized restoring access to critical business systems. Post-incident analysis led to the implementation of enhanced firewall configurations and network monitoring measures to prevent recurrence.

## Identify
- **Attack Type:** Distributed Denial of Service (DDoS) using ICMP flooding  
- **Affected Systems:** Entire internal network infrastructure, including systems critical for service delivery and internal operations  
- **Vulnerability Exploited:** Firewall misconfiguration that allowed unchecked ICMP traffic from external sources  
- **Business Impact:** Disruption to core services including web design, marketing operations, and client communication

## Protect
To improve defenses against future attacks:
- A rate-limiting firewall rule was added to control ICMP traffic volume  
- Source IP address verification was enabled to identify and block spoofed requests  
- An IDS/IPS system was deployed to flag and filter suspicious ICMP behavior  
- Internal processes were updated with refreshed security policies and training protocols for IT staff  
- Scheduled firewall audits were introduced to ensure continuous alignment with best practices

## Detect
To increase early detection capabilities:
- Network monitoring software was installed to flag traffic anomalies, especially abnormal ICMP traffic patterns  
- The firewall was configured to log and alert on spoofed IP addresses  
- IDS sensors were fine-tuned to detect traffic characteristics typical of ICMP flood attacks  
- Plans were made to introduce a Security Information and Event Management (SIEM) platform for centralized threat correlation and alerting

## Respond
The organization developed a response strategy to contain and manage future incidents:
- Isolate affected systems quickly to prevent lateral disruption  
- Prioritize recovery of critical services while non-essential functions remain offline  
- Analyze firewall and IDS logs for signs of malicious behavior and traffic origins  
- Communicate incident details to IT teams, leadership, and stakeholders promptly  
- Document findings and adjust incident response playbooks accordingly

## Recover
To restore normal operations after a DDoS incident:
- Immediately block malicious traffic at the firewall  
- Temporarily suspend non-essential services to conserve bandwidth and system resources  
- Restore critical network services first to ensure business continuity  
- Gradually reintroduce non-critical systems after verifying that attack traffic has ceased  
- Conduct a review of recovery actions to inform future improvements and update documentation

## Reflections/Notes
This incident highlights the importance of proactively managing firewall configurations, monitoring inbound traffic, and having clear response and recovery strategies. Ongoing assessments and training will support continuous improvement of our cybersecurity posture.
