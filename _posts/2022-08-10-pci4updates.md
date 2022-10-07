---
layout: post
title: PCI DSS v4.0 Global Symposium
subtitle: Detailed notes from the Global Symposium published in July of 2022
date:   	2022-08-10
tags: [SecurityProgram, ITAudit]
comments: false
---

## PCI DSS v4.0 Global Symposium - Introduction

In July of 2022, PCI released the [PCI DSS v4.0 Global Symposium](https://events.pcisecuritystandards.org/pcidss4-0-global-symposium?utm_campaign=2021%2520Community%2520Meetings), which provided in-depth coverage of what is new in version 4.0 of the standard. This three-hour-long presentation provided a great deal of depth in a condensed format, saving the viewer from having to thoroughly read through all the updated documentation.

The symposium also added a lot of clarification on PCI’s perspective and intent behind many of the new requirements, that might not easily be gleaned from reading the updates on your own.

PCI DSS v4.0 has been expanded in its philosophy to also be utilized to protect against threats and secure other elements of the payment card ecosystem beyond the Card Data Environment (CDE). As the payment industry continues to evolve, PCI has worked towards a more broad framework that can be used as an effective security baseline across fintech infrastructure.

{: .box-note}I have taken detailed notes from the entire session for future reference. If you happened upon this page, via Linkedin or Google Search, please hop over to [LinkedIn](https://www.linkedin.com/in/speden/) to say hi and be sure to connect with me!


### PCI DSS v4.0 Update Highlights

PCI has published a [Summary of Changes](https://docs-prv.pcisecuritystandards.org/PCI%20DSS/Standard/PCI-DSS-v3-2-1-to-v4-0-Summary-of-Changes-r1.pdf) document on its [Document Library](https://www.pcisecuritystandards.org/document_library/?category=pcidss&document=pci_dss) page. Please reference this document in addition to the notes I have captured from the PCI DSS v4.0 Global Symposium.

The 12 PCI requirements are now referred to as the 12 Principal Requirements. Some wording has changed to help better specify the intent of the requirements, but the security objectives remain the same.

Some key updates include:

* **Requirement 1** has been updated firewall terminology to more broadly address network security controls to support the broader range of technologies traditionally met by firewalls.
* **Requirement 2** has been officially expanded beyond addressing vendor-supplied defaults to address secure configuration management more broadly.
* **Requirement 3** has been expanded to emphasize that account data and not just cardholder data needs to be protected
* **Requirement 4** has been modified to add more specific requirements around the use of strong cryptography.
* **Requirement 5** has been updated to clarify that both systems and networks need to be protected from malicious software.
* **Requirement 6** has been updated to emphasize software rather than applications
* **Requirement 7** has been updated to require that access needs to be restricted for both system components and cardholders on a need-to-know basis
* **Requirement 8** has not had significant changes.
* **Requirement 9** has not had significant changes.
* **Requirement 10** has more specifically required that access be logged (and not simply tracked) and has been expanded to also include logging of access to system components.
* **Requirements 11** was been expanded to require the security testing of both system components and networks regularly.
* **Requirement 12** has been updated to better define the overarching goal of both security policies and procedures.


### PCI DSS Applicability Information

PCI has updated its applicability information to add additional clarity around which entities the standard is addressed to. Some key modifications added in version 4.0 include:


* PCI DSS is intended for entities that store, process or transmit cardholder data and/or sensitive authentication data **AND**
* Entities that could impact the security of the cardholder data environment

{: .box-warning} Note that PCI restates that Sensitive Authentication Data (SAD) is never permitted to be stored, even if Primary Account Numbers (PAN) are not present. PCI DSS also applies to organizations that transmit or process SAD and are also required to comply with PCI DSS 4.0.


### Updated PCI DSS Definitions

PCI has simplified the definition of multiple key terms including Cardholder Data, Card Data Environment, and Sensitive Authentication Data

**Cardholder Data (CHD) includes:**

* Primary Account Number (PAN)
* Cardholder Name
* Expiration Date
* Service Code (The Service Code is a 3-digit value encoded into the magnetic stripe on the back of your credit and debit cards.)

**Sensitive Authentication Data (SAD) includes:**

* Full track data (magnetic stripe data or equivalent data on a chip)
* Card verification code
* PINs/PIN block

**Card Data Environment (CDE) includes:**

* System components, people, and processes that store, process, and transmit CHD and/or SAD
* System components that may not store, process, transmit CHD or SAD but have unrestricted access to system components that do store, process, transmit CHD or SAD
* System components, people, or processes that could impact the security of the CDE.


{: .box-warning} **PCI Terms are Not Interchangeable**:  PCI has also reinforced its use of different terms for different types of data processed during payment card transactions. Different terms are purposely used to provide context around the security requirements required for the various data elements present in payment card transaction processing. <br>For example- if PCI DSS states that the PAN needs encrypted, they are only requiring encryption of PAN and not the broader family of cardholder data.

**Relationship between PCI DSS and PA DSS**

PA DSS is being deprecated in favor of the PCI Software Security Framework PCI SSF can be leveraged in conjunction with requirement 6 of PCI DSS as needed.

**Bespoke and Customer Software**



* Bespoke software is defined as software developed by a 3rd party to the organization’s specific specifications.
* Customer software is defined as software developed by the organization for its use.


### Expansion of Rogue Wireless Detection Requirements

PCI requires rogue wireless detection even when wireless is not used within the CDE, and a policy prohibits the use of wireless devices.

Encrypted Cardholder Data and Impact to PCI DSS Scot of Third Party Service Providers

If a third party receives encrypted data and cannot decrypt the data, it may be provided out of scope.

**Use of Third-Party Service Providers (Requirement 12.8)**


* Third parties do not need to be PCI DSS certified for the assessed org to become certified
* If a third party is used to meet a PCI requirement, the organization cannot be compliant without the third party also demonstrating they meet the requirements. Their compliance need to be validated via their AOC, or via the audit extending to the third party (on-demand assessment).
* The Third-Party Service Provider's evidence of compliance can be obtained via the Payment Brand List(s) of PCI DSS Compliant Service Providers if it is clear that the certification is related to the services used.

**Sampling for PCI DSS Assessments**


* If automated processes are in use, 100% of the population should be used if possible
* If an automated process cannot be utilized, sampling is an option based on the assessor’s discretion.

**Frequency Expected for Timeframes called out in PCI DSS Requirements**

PCI DSS has updated the standard to allow organizations to set their timelines for completing some tasks based on the business needs and risks relevant to the organization.

PCI expects organizations to document their timeframes in policies and procedures, and adhere to them. The assessor’s job will be to verify completion per company policy.

Organizations need to perform activities as close to the specified interval without exceeding it.


### Approaches for Implementing and Validating PCI DSS

Organizations now have two approaches for implementing and validating PCI DSS. Organizations now have more flexibility in demonstrating compliance and obtaining certification.



* Defined Approach: Follows current PCI DSS requirements and the testing procedures provide a defined methodology for meeting all security objectives.
* Customize Approach: This new approach allows the organization to develop its controls to meet the security objectives. This approach should only be undertaken by a mature organization with well-established security programs. This approach is more appropriate for organizations utilizing newer technologies. The updated PCI DSS standard provides two appendices with templates to follow to complete the customized approach.


## PCI DSS 4.0: Impactful Changes

All changes are included in the Summary of Changes document. This section only details the most impactful changes.

**Overarching Changes to Be Mindful of:**

**Guidance vs Requirements - **Guidance clarifies requirements but doesn’t define them. Guidance may now provide some examples of technologies used, or approaches to meeting requirements, but it is not PCI’s defined approach to meeting a requirement.

**Targeted Risk Analysis: **This allows for a customized, risk-based approach to meeting a requirement. Some requirements now allow the business to define the frequency that the Control is performed instead of the standard defining it.

**Customized Approach: **This is a type of targeted risk analysis that allows for more flexibility in meeting a requirement with emerging technology.

**Roles and Responsibilities: **The updated standard now requires formally defining the roles and responsibilities required to perform various tasks and controls to meet the requirements.


### Requirement 1 Updates:

There are no new requirements but there are some impactful clarifications.



* Networking Changes must be made per requirement 6 formal change management controls.
* Configuration Files must be secured and kept consistent, even in cloud environments.
* Network Security controls must be in place between a wireless network and a cardholder data environment, even if the wireless network is part of the CDE.

**Trusted vs Untrusted Networks**

As networking technologies have evolved, PCI has evolved the standard to focus on the development of Trusted Networks and Untrusted Networks.



* Trusted Network: Networks you control or manage, with PCI DSS controls applied
* Untrusted Network: Networks you can’t control or manage, and/or PCI DSS controls are not applied. (Can include both networks owned and not owned by the organization.

**Use of DMZs: **A DMZ is still a best practice but not explicitly required.


### Requirements 2 Updates:

Additional clarity has been provided around the relationship between system components and their functions. Additional flexibility is provided to allow for complying.



* Separating System Components Functions: It has always been a PCI DSS requirement that different functions shouldn’t be co-located on the same server if it would result in one of the services being required to operate at a lower security profile. PCI DSS now allows for multiple system components to be co-located on a single system if:
    * If functions with different security levels are isolated
    * If isolation isn’t possible, all functions operate at the maximum security level
* Vendor Default Account Password Changes must be managed per password management requirements in Requirement 8
* Configuration Standards now must be updated as vulnerability issues are identified per the vulnerability management requirements identified in Requirement 6.
* Security Settings and Parameters need to be explicitly addressed when establishing system configuration standards, to identify where steps are being taken to set parameters that reduce the attack surface and apply the least privilege. It is recommended to rely on industry hardening guidance for implementing secure configurations.
* The System Component Inventory that defines all in-scope system components has been moved to requirement 12.


### Requirement 3 Updates:

Changes in Management of SAD:



* The data retention policy must address the storage of Sensitive Authentication Data before it is used for authorization.
* Sensitive Authentication Data must also be encrypted if stored electronically before the completion of authorization.

Restrictions on Copy/Paste in Remote Access Sessions:



* Technical controls need to be implemented to prevent the copy and paste of Primary Account Data when using remote-access technologies.

Changes in Encryption Requirements:



* Disk and partition level encryption is only permitted on removable media.
* File, column, or field level database encryption is required to render all PAN unreadable, with exception of removable media. If this is not possible, other approaches must be considered.

Updates to Cryptographic Key Use Rules:



* For service providers using separate test and production environments, it is prohibited to use the same cryptographic keys in both environments.
* Where hashing is used to render PAN unreadable, key cryptographic hashes, rather than simple one-way hashes are required, using a key-management process.
* Where hashing is used, hashing should use a Keyed Cryptographic Hash to prevent brute force guessing of the secret used to hash PAN and reverse the hash. This is means to prevent brute force attacks on a small number of hashes, the discover the single secret used to hash a large population of PAN. This is different from Saltinng which is used to protect large pre-calculated tables of hashes. Keyed cryptographic hashing also helps protect small populations of hashes, where cracking one hash may allow cracking them all.


### Requirement 4 Updates

Requirement 4 includes updates surrounding protecting PAN during transmission.



* Self-signed certificates need to be produced using an internal certificate authority within the organization. The certificate’s author will need to be confirmed and cannot be expired.
* An inventory of certificates in use also needs to be developed and maintained. Each certificate in use will also need to detail the algorithm used and expiration date.


### Requirement 5 Updates:



* Malware scanning may now be behavioral-based instead of signature-based.
* Entities now have more flexibility over determining how often malware scans and system component evaluations are completed based on targeted risk analysis.
* Anti-malware measures are also required for external media (USB drives).
* Anti-phishing technical controls are now required to prevent phishing attacks. The technical element is in addition to, and not an alternative to, Phishing awareness training.


### Requirement 6 Updates:



* Organizations must now maintain an inventory of bespoke and custom software to ensure it is also covered by patch management controls.
* Automated security scanning must now be implemented on all public-facing web applications to continually detect and prevent web-based attacks (Note, this requirement replaces a prior option to manually perform manual vulnerability testing of applications).

New e-Commerce Requirements to Address Skimming Attacks

This is referring to the skimming of single data transactions via an e-commerce transaction taking place on a payment page. Ideally, there should be no scripts located on a payment page that is not related to processing payments.



1. All payment page scripts (i.e., any script included on a payment page including those not related to processing payment transactions) loaded and executed on the consumer’s browser must be protected through the implementation of three controls
    1. A method must be implemented to ensure that all payment page scripts are authorized.
    2. A method must be implemented to ensure the integrity of each script.
    3. An inventory of all scripts must be maintained and justification must be provided as to why each is necessary.


### Requirement 7 Updates:

Requirement 7 expands its focus on access control governance over databases that may contain cardholder data to any queryable repositories and related system components.

For all systems within the CDE and systems impacting its security,



* Access to all system components must be appropriately defined and assigned.
* Expand access reviews to all application and system accounts, and related access privileges
* Service Accounts (Service and Application Accounts) must be explicitly limited to applicable systems and processes assigned to them.


### Requirement 8 Updates:



* Group, shared, or generic accounts may now be used on an exception basis by development teams if the use is managed under exceptional circumstances, and for a limited period. All actions taken under a shared account must still be attributable to an individual user.
* Passwords and passphrases requirements have shifted (check the standard for details).
* Passwords no longer need to be rotated every 90 days if Multi-factor authentication is in use on the system. For systems only protected passwords, rotation must take place every 90 days OR the organization may implement dynamic analysis tools.
    * Dynamic Analysis tools in Access Control consider additional access variables including user location, time, and Device Integrity, as part of the authentication method to determine if a password may be compromised.
* Multifactor authentication must be implemented for gaining access to the CDE for users both internal and remote access. MFA only needs to be applied once (e.g., to access the network, or individual systems, but not both)
* Interactive login for Service Accounts (Service and Application Accounts) must be managed.


### Requirement 9 Updates



* Target risk analysis may be used to determine how often POI devices are inspected.


### Requirements 10 Updates

Note that logging requirements also apply to user activities by employees, vendors, etc but do not apply to users or card holders.



* Target risk analysis needs to be used to define log review frequency.
* Automated log reviews will be required by March 31, 2025.


### Requirement 11 Updates



* Non-critical and not high-risk internal vulnerability scannings must be addressed, and internal scans must use authenticated scanning to allow for deeper inspection of systems and services not publicly available to the scanner.
* Service providers must provide the users of their systems with IDS/IPS and detection solutions, and alert users of the system of potential covert malware communication channels.
* E-commerce skimming detection controls must be implemented to detect changes or tampering with code on payment pages. The anti-skimming control must also ensure that malicious activity is not taking place at the time the script is constructed. This does not mean that merchants are required to install security controls on the end-user system. Content Security Policies and script-src directives are the preferred way to implement this requirement.


### Requirement 12 Updates



* A targeted risk analysis will be required to define and justify the frequency each control PCI has allowed flexibility in the frequency that the control is operated. These controls will have a frequency requirement defined as “periodically” within the standard.
* A targeted risk analysis is also required for every custom approach an entity wishes to use to satisfy a control.
* Service providers must support customer requests to address requests regarding the compliance with controls they are performing on behalf of their customers.
* The organization must also perform reviews of the cryptographic cipher suites and protocols in use at the organization.
* There is a new scope confirmation requirement as well. The PCI DSS scope must be formally reviewed, documented, and approved. Service providers must perform this exercise every 6 months.
    * Scope verification must include documenting
        * Data Flows for all applicable payment stages (e.g., authorization, settlement, chargebacks, refunds, and payment channels),
        * updating data flows for network security controls, identifying all locations where card data is stored (e.g., applications that process card data, file backups, transmissions between systems)
        * All system components within the CDE, connected to the CDE, or could impact the security of the CDE
        * 3rd party vendors with connections to the CDE
        * All segmentation controls are in place to create the logical boundary around the CDE.
* The security awareness program needs to be updated at least once a year. Security awareness must also include training around phishing awareness training.


## Flexibility for Implementing Security Controls and Validating Requirements

Within the new version of PCI DSS there are now three ways an organization can select security controls to help them become compliant:



* Defined approach with predictable requirements - similar to the prior version of PCI DSS
* Compensating Controls allow organizations flexibility when they can’t meet a standard and need to use an equal but alternative control
* A customized approach is for those with the expertise to develop a risk-based, non-traditional control meant to be applied to newer technology. Its focus is on meeting the objectives of the requirements as opposed to the defined methodology provided by the PCI DSS.

You can mix and match your approach down to the sub-requirement level. The goal is that the level of security is met, regardless of the control that has been implemented.


## How to use the PCI DSS Customized Approach

PCI DSS version 4 allows organizations to use a customized approach to meeting PCI DSS requirements, all the way down to the individual sub-requirement level. This allows the organization to define its methodology for showing compliance with the requirement based on its Objective, as opposed to being required to show compliance through adherence to the defined methodology prescribed by the Defined Approach.

To take advantage of the customized approach, the organization must take a few steps to document the control.



1. Document the customized control and how the control meets the PCI requirement’s Objective. Document this within the Organization’s Control Matrix - See PCI DSS Appendix E1
2. Perform a Targeted Risk Analysis and document the risk analysis within PCI DSS Appendix E2
3. Describe the testing the organization performed on the custom control and document test results within PCI DSS Appendix E1
4. Describe how the control is maintained and how ongoing effectiveness is assured. Also document this within PCI DSS Appendix E1.

The assessor will be responsible for reviewing the documentation to understand the customized control, ensure its properly documented, and verify it meets the security requirements of the PCI DSS Objective.

The assessor then has to develop their testing procedures for the custom control, which must provide sufficient evidence to demonstrate that the control is operating. The assessor must document everything within Appendix E as well.


### Understanding the difference between PCI’s Customized Approach and Compensating Controls

PCI’s customized approach is meant to meet different needs of the organization from the compensating controls approach.

Compensating controls are meant for entities that cannot meet a requirement due to a technical or business restraint. This allows the organization to implement an alternative control to mitigate the risk. A simple example may be a company using a payments application solution that currently only supports a version of TLS/SSL not allowed by PCI. The compensating control may be encapsulating all that application’s traffic within a VPN to provide a sufficient level of TLS to meet PCI requirements. These controls are most commonly used for legacy applications.

The customized approach is meant to allow organizations with mature risk-management practices to implement different controls that meet the Customized Approach Objective in a different way than the defined requirement. Appendix D and E provide information and templates to support the implementation of a customized approach.


## Explanation of Report Findings


### In Place with Remediation

This is a new reporting option where the entity was found to have a failing control during a PCI assessment but remediated before the end of the assessment.

Examples:



* Security patches not applied within 30 days
* A misconfigured network security control
* Users that missed security awareness training
* Accidental storage of unencrypted PAN
* A missing quarterly vulnerability scan

This finding is not meant to ding an organization for minor issues such as missing signatures or review of documents.


### Difference between Not Applicable and Not Tested

The Not Applicable finding type requires the assessor to document the testing performed to confirm the not applicable status of the control. For example - if a control is not applicable because no PAN exists in an environment, the assessor would be expected to document how that was determined.

The Not Tested finding type indicates that no testing was performed and the assessor does not know whether the requirement applies or is in place. This would only be used if an acquirer or other upstream entity defined the specific scope for an organization to complete. For example:



* Acquirer asks the merchant to include only Prioritized Approach Milestones 1-4 in their assessment
* An organization only includes the requirements for a newly implemented technology in their assessment
* A service provider includes only requirements for a data center hosting service in the assessment.

This cannot be used as a means for the organization to simply scope out items they don’t wish to show up in the Assessment.


## New Reporting Options at PCI DSS 4.0

Within the Overall Assessment Results there are now two assessment options and three overall assessment result options available:

**Assessment Options:**



* Full Assessment - all requirements assessed and passed
* Partial Assessment - allows for not completing all sections of PCI DSS, but must require an explanation for why sections have not been tested.

**Assessment Result Options:**



* Compliant - All sections were completed and findings were either In Place with Remediation, Not Applicable, or In Place, resulting in a compliant status.
* Non-Compliant - Not all sections were completed, or one or more requirements were marked as not in place.
* Compliant But With Legal Exception - This is used if the requirement cannot be met because meeting it would violate a law or regulation. Note that contractual obligations or legal advice do not suffice as legal or regulatory requirements.

This means an organization can now have a compliant status without completing all the requirements of PCI DSS 4.0. This was not possible in prior versions of PCI DSS.


## Updates to Findings and Observations

PCI has shifted its expectations away from writing long testing narratives or repeating the same narratives over and over in favor of relying more on references back to evidence and work papers.

**For each requirement the assessor will now be able to:**



* Provide one consolidated assessor narrative to describe how they concluded the organization was compliant with the requirements. The narrative should describe the work papers and evidence reviewed, and how the conclusions were made. PCI is not looking for a regurgitation of the defined requirements. If a customized approach was taken, this needs to be described in detail.
* For each test, identify/reference evidence rather than the detailed report results
* Select one of five checkboxes to determine the assessment findings and a sh
* Indicate via checkboxes which approach was taken to test the requirement (i.e., defined vs customized)


### Expectations for Writing Narratives at the Sub-Requirement Level

When completing the Reporting Details attached to each individual sub-requirement, PCI only expects to see the documentation reference number relating to the documentation reviewed to draw your conclusions.


### Changes to Self Assessment Questionnaires at PCI DSS v4.0

At PCI DSS 4.0, there are still eight SAQs for merchants and one for Service Providers.


## Summary of Changes for SAQs for Merchants



* Additional guidance has been added to the SAQs to make the expectations clear.
* SAQs have also been aligned more closely with the Report on Compliance, including the detailed guidance, testing procedures, and applicability notes.
* The wording in SAQs now reflects the language used in PCI DSS.

**SAQ A Key Changes:**



* Manage all payment page scripts
* Minimum password lengths increase to 12 characters
* Change and tamper detection mechanisms must be in place for payment pages
* Quarterly ASV scanning is now required.

**SAQ A-EP**



* Conduct targeted risk analysis of systems impacting payment card processing
* Protections against phishing
* Maintain an inventory of bespoke and 3rd party software components
* Automated log reviews
* Implementation of MFA into the CDE
* Implementation of Security Awareness Training (including Phishing awareness training)

**SAQ B**



* Policies and procedures must include policies and procedures regarding the protection of stored account data

**SAQ B-IP**



* Policies and procedures must include policies and procedures regarding the protection of stored account data and restricting physical access to cardholder data

**SAQ C**



* Must establish policies and procedures over its payment card protection requirements
* Perform targeted risk analysis over systems impacting payment card processing
* Implementing phishing protections and Security Awareness Training
* Implement Secure Software Development processes and procedures
* Implementation of MFA into the CDE
* Ensure proper time synchronization is in place and logging of the CDE is implemented and sufficiently protected.

**SAQ C-VT**



* Must establish policies and procedures over its payment card protection requirements
* Malware scans on removable media must be implemented on terminals being used to enter card data
* Technical protections against phishing must be implemented
* Security awareness training must be implemented

**SAQ P2PE**



* Must establish policies and procedures for the protection of stored account data and restrict physical access to cardholder data.

**SAQ D**

This includes all PCI DSS requirements and is effective immediately for all PCI 4.0 assessments.
