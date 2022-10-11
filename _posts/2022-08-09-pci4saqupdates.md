---
layout: post
title: Changes to Self Assessment Questionnaires at PCI DSS v4.0
subtitle: Detailed notes from the Global Symposium published in July of 2022
date:   	2022-08-09
tags: [SecurityProgram, ITAudit]
comments: false
---

## Changes to Self Assessment Questionnaires (SAQs) at PCI DSS v4.0

{: .box-note}
**Quick Introduction** <br>In July of 2022, PCI released the [PCI DSS v4.0 Global Symposium](https://events.pcisecuritystandards.org/pcidss4-0-global-symposium?utm_campaign=2021%2520Community%2520Meetings), which provided in-depth coverage of what is new in version 4.0 of the standard. This three-hour-long presentation provided a great deal of depth in a condensed format, saving the viewer from having to thoroughly read through all the updated documentation.<br><br>I have taken detailed notes from the entire session for future reference. Also check out my [overview of critical updates in PCI DSS 4.0](https://shanepeden.github.io/shanepeden.com/2022-08-10-pci4updates/).


### Changes to Self-Assessment Questionnaires at PCI DSS v4.0

At PCI DSS 4.0, there are still eight SAQs for merchants and one for Service Providers, but there are multiple updates to SAQs including the addition of multiple new requirements to the questionnaires.

In this post we will cover the updates to the PCI DSS 4.0 Self-Assessment Questionnaires (SAQs). Please see the PCI Security Standards Council's documentation on [Understanding the SAQs for PCI DSS](https://www.pcisecuritystandards.org/document_library/?category=pcidss&document=pci_dss) and download the latest SAQs from PCI's [document library](https://www.pcisecuritystandards.org/document_library/?category=pcidss&document=pci_dss).

## Summary of Changes for PCI DSS 4.0 SAQs for Merchants

* Additional guidance has been added to the SAQs to make the expectations clear.
* SAQs have also been aligned more closely with the Report on Compliance, including detailed guidance, testing procedures, and applicability notes.
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
* Must establish policies and procedures for its payment card protection requirements
* Perform targeted risk analysis over systems impacting payment card processing
* Implementing phishing protections and Security Awareness Training
* Implement Secure Software Development processes and procedures
* Implementation of MFA into the CDE
* Ensure proper time synchronization is in place and logging of the CDE is implemented and sufficiently protected.

**SAQ C-VT**
* Must establish policies and procedures for its payment card protection requirements
* Malware scans on removable media must be implemented on terminals being used to enter card data
* Technical protections against phishing must be implemented
* Security awareness training must be implemented

**SAQ P2PE**
* Must establish policies and procedures for the protection of stored account data and restrict physical access to cardholder data.

**SAQ D**
* This includes all PCI DSS requirements and is effective immediately for all PCI 4.0 assessments.



 {: .box-note}
 **Have More Questions? Let's Connect!** <br>I've helped dozens of companies prepare for PCI DSS, ISO 27001, HITRUST, SOC 2, and more! If you have any questions, please hop over to [LinkedIn](https://www.linkedin.com/in/speden/) to say hi and be sure to connect with me! <br><br>If you're in the Atlanta area, [we can also grab a coffee](https://shanepeden.github.io/shanepeden.com/aboutme/)!
