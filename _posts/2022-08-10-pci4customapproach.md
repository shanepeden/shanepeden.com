---
layout: post
title: How to use the PCI DSS Customized Approach
subtitle: Detailed notes from the Global Symposium published in July of 2022
date:   	2022-08-09
tags: [SecurityProgram, ITAudit]
comments: false
---

## PCI DSS v4.0 Global Symposium - Introduction

In July of 2022, PCI released the [PCI DSS v4.0 Global Symposium](https://events.pcisecuritystandards.org/pcidss4-0-global-symposium?utm_campaign=2021%2520Community%2520Meetings), which provided in-depth coverage of what is new in version 4.0 of the standard. This three-hour-long presentation provided a great deal of depth in a condensed format, saving the viewer from having to thoroughly read through all the updated documentation.

In this post, we will cover PCI DSS's new customized approach option, and highlight clarifications on how and when compensating controls should be used.

{: .box-note}
**Let's Connect!** <br>I have taken detailed notes from the entire session for future reference. If you happened upon this page via Linkedin or Google Search, please hop over to [LinkedIn](https://www.linkedin.com/in/speden/) to say hi and be sure to connect with me!


### How to use the PCI DSS Customized Approach

In PCI DSS version 4, organizations have a new option for demonstrating compliance, referred to as the customized approach.

The customized approach allows organizations to define their controls and methodology to demonstrate compliance with PCI DSS requirements, all the way down to the individual sub-requirement level of the standard. In these situations, the organization is demonstrating how it meets a requirement's objective, as opposed to being required to demonstrate compliance through adherence to the defined methodology prescribed by the Defined Approach.

The customized approach is most successful when the organization has mature security processes and strong risk management practices in place. The organization must be able to effectively design, document, test, and maintain security controls to meet the objective.

#### Requirements for Implementing PCI DSS 4.0's Customized Approach
When utilizing the PCI DSS's customized approach, there are several steps the organization must take:

1. Document the customized control and articulate how the custom control meets the requirement’s Objective within the Organization’s Control Matrix - See PCI DSS Appendix E1
2. Perform a Targeted Risk Analysis (per requirement 12.3.1) and document the risk analysis within PCI DSS Appendix E2
3. Describe the testing the organization performed on the custom control and document test results within PCI DSS Appendix E1
4. Describe how the control is maintained and how ongoing effectiveness is assured. Also document this within PCI DSS Appendix E1.

The assessor will be responsible for reviewing the documentation to understand the customized control, ensure it is properly documented, and verify it meets the security requirements of the PCI DSS Objective.

The assessor then has to develop testing procedures for the custom control, which must provide sufficient evidence to demonstrate that the control is operating. The assessor must document everything within Appendix E as well.


### Understanding the difference between PCI’s Customized Approach and Compensating Controls

There is a distinct difference between PCI’s customized approach and compensating controls that merit clarification. Each is intended to meet the different needs of the organization.

**Compensating Controls**
* Compensating controls are for entities that cannot meet a requirement due to a technical or business restraint. The compensating control allows the organization to implement an alternative control to mitigate the risk.
 * A simple example is company using a payments application solution that currently only supports a version of TLS/SSL not allowed by PCI. The compensating control may include implementation of a VPN to protect the traffic, providing a sufficient level of TLS to meet PCI requirements.
Compensating controls are used often in legacy applications.

**Customized Approach**
* The customized approach allows organizations with mature risk-management practices to implement custom controls that meet the Customized Approach Objective. The approach may be completely different from the defined requirement.
 * PCI DSS Appendix D and E provide information and templates to support the implementation of a customized approach.


 {: .box-note}
 **Have More Questions? Let's Connect!** <br>I've helped dozens of companies prepare for PCI DSS, ISO 27001, HITRUST, SOC 2, and more! If you have any questions, please hop over to [LinkedIn](https://www.linkedin.com/in/speden/) to say hi and be sure to connect with me! If you're in the Atlanta area, [we can also grab a coffee](https://shanepeden.github.io/shanepeden.com/aboutme/)!
