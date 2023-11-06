# NIST-Compliance
NIST 800-53 PIC OR SOMETHING HERE

# Introduction
In this project, I remediate my mini honeynet I created in the previous project (Building a SOC + Honeyet), to be up to par and compliant with NIST SP 800 53 R5 regulatory compliance standards. I resolved several non-compliant controls within the security metrics in Microsoft Azure to harden the environment and decrease/nullify attacks as well as keeping the environment up to compliant standards.  The compliance metrics we will mitigate and audit are:

- AC: Access Control
- AU: Audit and Accountability 
- CP: Contingency Planning
- IA: Identification and Authentication
- IR: Incident Response
- RA: Risk Assessment
- SC: System and Communications Protection
- SI: System and Information Integrity


## Ratings Before Hardening/Security Controls

[SHOW MAIN PICTURE]

## Metrics Before Hardening /Security Controls

Some of the more common compliance issues were the lack of encryption & having email notifications for security alerts/
[SHOW ERROR PICS 1]

In addition to regular compliance issues there were “Quick Fixes”, such as Microsoft defender being enabled for different sources to match approved compliant status, with a HIGH severity.

[SHOW ERROR PICS 3]

[SHOW ERROR PICS 3.5]

Each compliance tool had different freshness intervals as well from the lower end 30 minutes to 24 hours to verify compliance approval. 



# IMPLEMENTATION:

We started with the AC: Access control compliance controls with AC: 2 and ended with putting the SC: System and Communications Protection to compliance. Throughout I implemented both the Manual option options as well as Quick Fix & exemption tools when applicable.  

[SHOW quick logic v manual PIC]

[SHOW EXEMPTION 1 PIC]

Some Of The Common Remediation Functions To Fix:
- Firewall Creations for VMs (linux/Windows)
- Email Notifications
- Exemptions
- Enabling of Microsoft defender for resource manager, DNS, etc. 
- Azure Backup for virtual machines
- Purge Protection
- Subnets associated with network security groups


Some Of The Common Techniques (categories) Fixed during remediation.
- Defense Evasion (https://attack.mitre.org/tactics/TA0005/)
- Privilege Escalation
- Impact (https://attack.mitre.org/tactics/TA0040/)
- Persistence (https://attack.mitre.org/tactics/TA0003/)
- Exfiltration (https://attack.mitre.org/tactics/TA0011/)
- Lateral Movement (https://attack.mitre.org/tactics/TA0008/)






## Ratings AFTER Hardening/ Security Controls

The metrics shown below is after 24 hours of our last policy edit, showing increase in not only the NIST framework but also in the Microsoft Cloud security Benchmark controls as well. 

[SHOW COMPLIANCE AFTER 4 PIC]

## Metrics AFTER Hardening/ Security Controls

As shown below majority of all compliance policies were mitigated

[SHOW COMPLIANCE AFTER 5 PIC]

# Conclusion

In this project, NIST SP 800 53 R5 policy changes were made within the Azure environment to become more compliant with regulations. Utilizing the tools available we were able to create firewalls for our virtual machines, create backups for virtual machines, create subnets with our NSGS, enable Microsoft Defender for several resources and more. It is noteworthy that the number of security events and incidents were drastically reduced after the security controls were applied, demonstrating their effectiveness (as shown in previous Azure SOC + Honeynet lab)


It is worth noting that remediating the environment to be more compliant with NIST SP 800 53 5 also increased our compliance with the Microsoft Cloud Security Benchmark (Azure default), increasing our overall score to a whopping 88% Secure Score!

[SHOW PIC SECURITY POSTURE 3]



