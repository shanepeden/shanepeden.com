---
layout: 	post
title:  	Clinical treatment of ransomware in healthcare
subtitle: 	Originally Posted in Security Magazine
date:   	2021-06-09
author: 	Shane Peden
header-img: img/blueheader.jpg
catalog: 	true
tags:
    - SecurityProgram
    - healthcareIT
    - HacksAndAttacks
---

Healthcare organizations experience constant tension between two priorities: improving patient care, and controlling costs. To find the proper balance and focus on both of these priorities, healthcare organizations have to focus on providing positive experiences, managing resources, and innovating technology.

At the same time, a myriad cyber-related threats plague healthcare organizations, with few of greater concern than ransomware. For a healthcare organization, the ramifications of a cyberattack expand beyond financial harm. Cyber-attacks have the potential to inhibit the organization's ability to provide care. These attacks also have regulatory compliance, and legal impact as they may constitute a breach under HIPAA or result in medical malpractice. This may result in additional audits, fines, and other burdens on the organization.

In 2020, at least 92 US healthcare organizations suffered ransomware attacks, resulting in an average ransom demand of $169,446 and netting cybercriminals an estimated $15.6 million in ransoms demanded from the US healthcare sector.

## Understanding Why Health Systems Are An Attractive Target for Ransomware

Cybercriminals often focus their attacks on the most vulnerable targets, and unfortunately health systems tend to be high on that list. Since the introduction of the Meaningful Use program by the Center for Medicare & Medicaid Services (CMS) in 2011, the adoption of Electronic Health Record (EHR) solutions by hospitals had increased to more than 94% by 2014. Digital transformation in health systems accelerated even further over the pandemic. However, rapid change sometimes creates conflicting priorities leading to divergent and fragmented technologies within a single health system. This makes it easier for attackers to focus their attention and attacks. Additionally, a lot of healthcare platforms have focused on data portability and interoperability which has meant that security was not necessarily a top priority. All of these factors make healthcare an appealing target, and when you consider that health systems are likely to succumb to ransom-based attacks to protect data, it just encourages the attackers even more.

These issues are further punctuated by a vulnerability profile similar to ransomware victims in other industries, including:

* Lack of sufficient incident response planning and testing of incident response capabilities
* Lack of sufficient backups, including the security of backups to ensure the systems managing backup data are not also victim to ransomware
* Poor network segmentation and logical access management, resulting in the easy spread of malware across IT networks.
* Poor security patching practices, resulting in systems vulnerable to pre-built, easy to deploy malware that can easily take over the system
* Insufficient anti-malware and anti-spam solutions, and poor configuration management (e.g., no prevention of MS Office Macros, presence of insecure services or features)
* Poor perimeter defenses include web filtering and internet access controls
* Use of legacy and out of support systems and a failure to isolate these on networks where they are a necessity

## Finding the Key Points of Entry for Ransomware into Health Systems

Ransomware typically finds its way into healthcare systems one of three ways:

* Malicious websites that silently initiate an infection (e.g., malvertisement, drive-by downloads)
* Phishing emails containing malicious attachments which execute malware when opened
* Phishing emails containing malicious email links to sites containing the malware

## Mitigating the Risk of Ransomware Infections

While there is no single solution to secure an organization against ransomware, healthcare providers can implement a combination of tools and best practices to better secure their systems and decrease the likelihood of a successful attack. Leadership teams as well as network managers leading security and technology teams within the healthcare system should be asking (or answering!) these five questions:

**1. How are we securing our end users?**

User traffic should be filtered through a DNS-based content filter to minimize exposure to malicious domains and websites not appropriate for use at work. A next-generation AV solution should be implemented, and anti-spam/phishing solutions should be integrated into the corporate email solution. Systems should be configured to prevent common types of attacks from taking place (e.g., disable macros in Office files, disable Powershell, prohibit applications from running outside of predefined directories).

**2. Do we have an incident response and BCP/DR plan and is it tested regularly?**

A plan should be in place to back up critical data and infrastructure. Backups should be separate from all other IT systems. Access to backups should be tightly controlled and encrypted. Live backup testing should be documented to prove that IT can recover all critical systems within a business-defined recovery time objective.

**3. Are our IT networks truly segmented?**

Separate subnets or virtual LANs are not enough. Traffic flows between networks must be restricted. Malware originating on an end-user system should not be able to navigate to sensitive infrastructure.

**4. What is our organization’s security patching cadence?**

The easiest way for malware to spread is to identify out-of-patch systems with known vulnerabilities that have out-of-the-box exploits available. In these scenarios, even attacks of low sophistication can be successful. Systems must be kept up to date. If the use of out-of-service, or legacy systems is a necessity, they should be firewalled appropriately to mitigate risk.

**5.  How are we training our workforce?**

Are users trained on spotting suspicious emails, and not to click on links or open attachments from emails? Are users aware of how to report malicious activity? Are users made aware of acceptable use policies, why they exist, and the ramifications for not adhering to them? Do patients understand what is at risk?

No health system should have to decide between improving patient care or covering the high cost of an unexpected ransomware attack. Examine the health and wellness of your IT infrastructure—just like a patient—to prevent long-term issues down the line.

{: .box-note} Note: This post was originally published on June 9th, 2021 on [SecurityMagazine.com](https://www.securitymagazine.com/articles/95381-clinical-treatment-of-ransomware-in-healthcare).
