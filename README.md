# NIST-Compliance
NIST 800-53 PIC OR SOMETHING HERE

# Introduction
In this project, I remediate my mini honeynet I created in the previous project [(Building a SOC + Honenet)](https://github.com/EricMcclellan1/Cloud-Soc#building-a-soc--honeynet-in-azure-live-traffic) to be up to par and compliant with NIST SP 800 53 R5 regulatory compliance standards. I resolved several non-compliant controls within the security metrics in Microsoft Azure to harden the environment and decrease/nullify attacks as well as keeping the environment up to compliant standards.  The compliance metrics we will mitigate and audit are:

- AC: Access Control
- AU: Audit and Accountability 
- CP: Contingency Planning
- IA: Identification and Authentication
- IR: Incident Response
- RA: Risk Assessment
- SC: System and Communications Protection
- SI: System and Information Integrity


## Ratings Before Hardening/Security Controls

<img width="845" alt="Screenshot 2023-11-04 at 4 17 41 PM" src="https://github.com/EricMcclellan1/NIST-Compliance/assets/147299619/1195ab83-cb46-4e3d-820b-73c351696b17">


## Metrics Before Hardening /Security Controls

Some of the more common compliance issues were the lack of encryption & having email notifications for security alerts. as well as Microsoft Defender configuration/

![error pics 1](https://github.com/EricMcclellan1/NIST-Compliance/assets/147299619/f6a81dbe-7338-465a-80dc-bcb520669b82)


In addition to regular compliance issues there were “Quick Fixes”, such as Microsoft defender being enabled for different sources to match approved compliant status, with a HIGH severity. <br/>
![error pics 3](https://github.com/EricMcclellan1/NIST-Compliance/assets/147299619/a3e9fcc2-82c9-4a4a-8d63-0299683ce799)


![Exfilration](https://github.com/EricMcclellan1/NIST-Compliance/assets/147299619/b8b31f91-16a5-4e2f-aa90-30e61013433d)


Each compliance tool had different freshness intervals as well from the lower end 30 minutes to 24 hours to verify compliance approval. 


# IMPLEMENTATION:

We started with the AC: Access control compliance controls with AC: 2 and ended with putting the SC: System and Communications Protection to compliance. Throughout I implemented both the Manual option options as well as Quick Fix & exemption tools when applicable.  


<img width="1305" alt="quick logic v manual" src="https://github.com/EricMcclellan1/NIST-Compliance/assets/147299619/3b375e0d-e882-4e65-bc05-81101b455d42"> <br/>



<img width="1763" alt="exemption 1" src="https://github.com/EricMcclellan1/NIST-Compliance/assets/147299619/d579a74a-7d98-4754-bb1f-ebb416931d2f"> <br/>


⭐ Some Of The Common Remediation Functions To Fix: 
- Firewall Creations for VMs (linux/Windows)
- Email Notifications
- Exemptions
- Enabling of Microsoft defender for resource manager, DNS, etc. 
- Azure Backup for virtual machines
- Purge Protection
- Subnets associated with network security groups <br/>


⭐ Some Of The Common Techniques (categories) Fixed during remediation.
- Defense Evasion (https://attack.mitre.org/tactics/TA0005/)
- Privilege Escalation (https://attack.mitre.org/tactics/TA0004/)
- Impact (https://attack.mitre.org/tactics/TA0040/)
- Persistence (https://attack.mitre.org/tactics/TA0003/)
- Exfiltration (https://attack.mitre.org/tactics/TA0011/)
- Lateral Movement (https://attack.mitre.org/tactics/TA0008/)




## Ratings AFTER Hardening/ Security Controls

The metrics shown below is after 24 hours of our last policy edit, showing increase in not only the NIST framework but also in the Microsoft Cloud security Benchmark controls as well. 


![compliance after 4](https://github.com/EricMcclellan1/NIST-Compliance/assets/147299619/0f449244-a261-4130-bbff-14e58dfc2551)


## Metrics AFTER Hardening/ Security Controls

As shown below majority of all compliance policies were mitigated


![compliance after 5](https://github.com/EricMcclellan1/NIST-Compliance/assets/147299619/1370d86f-f69a-4c87-a8d8-7ee2a9757f5f)


# Conclusion

In this project, NIST SP 800 53 R5 policy changes were made within the Azure environment to become more compliant with regulations. Utilizing the tools available we were able to create firewalls for our virtual machines, create backups for virtual machines, create subnets with our NSGS, enable Microsoft Defender for several resources and more. It is noteworthy that the number of security events and incidents were drastically reduced after the security controls were applied, demonstrating their effectiveness [as shown in previous Azure SOC + Honeynet lab](https://github.com/EricMcclellan1/Cloud-Soc#building-a-soc--honeynet-in-azure-live-traffic)

It is worth noting that remediating the environment to be more compliant with NIST SP 800 53 5 also increased our compliance with the Microsoft Cloud Security Benchmark (Azure default), increasing our overall score to a whopping 88% Secure Score!


![security posture 3](https://github.com/EricMcclellan1/NIST-Compliance/assets/147299619/56d0fb8f-f693-4726-a168-565a1c3437b1)




