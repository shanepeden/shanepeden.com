---
layout: 	post
title:  	Breaking Down the SUNBURST Hack
subtitle: 	Tuesday Morning Grind, Ep 9
date:   	2020-12-29
author: 	Shane Peden
header-img: img/blueheader.jpg
catalog: 	true
tags:
    - HacksAndAttacks
    - Podcast
    - RiskAssessment
---

> Tuesday Morning Grind, Ep 9 - Breaking Down the SUNBURST Hack

<iframe width="560" height="315" src="https://www.youtube.com/embed/ClA8vsYaVOk" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Podcast Summary ##
The SUNBURST Hack is perhaps the biggest security headline of 2020, impacting organizations like SolarWinds, FireEye, and thousands of others. In this episode of TMG, Shane and Christian break down the SUNBURST Hack, how it happened, and what you can do about it.

## Breaking Down the SUNBURST Hack ##

#### Quick Overview of Sunburst and How We Got Here ####
+ In early December of 2020, FireEye disclosed that they were victim to a nation state that resulted in the theft of some 300 Red Team assessment tools.
+ Five days after FireEye's incident disclosure, SolarWind's shared its disclosure of a vulnerability within the [Orion network monitoring application](https://www.solarwinds.com/orion-platform).
	- FireEye is believed to have discovered the vulnerability as part of threat hunting activities related its own hacks.
	- The attack consists of a trojanized (i.e. backdoor) version of a legitimately distributed software update from Solarwinds.
+ This attack is special in that it was a meticulously implemented supply chain attack. Most attacks come through phishing or exploitation of vulnerabilities.

#### What is a Supply Chain Attack? ####
+ The Sunburst attack is special due to being a meticulously implemented supply chain attack.
	- Most attacks are delivered through phishing, or exploitation of vulnerabilities. The attack impacted the modes of legitimate service delivery. The [2013 attack on retailer, Target](https://www.zdnet.com/article/anatomy-of-the-target-data-breach-missed-opportunities-and-lessons-learned/) is another famous supply chain attack.
+ The Solarwinds attack targeted the software build and code signing infrastructure. Companies receiving the infected updates were presented with digitally signed, authentic software updates from Solarwinds as expected.
	- The malicious code may have been presented as a vulnerable software library. Vulnerable code appears to have been injected in steps over time to avoid detection. [read more here](https://thehackernews.com/2020/12/new-evidence-suggests-solarwinds.html)

#### What Makes Sunburst (and its dropper, Teardrop) so Formidable?  ####
+ Sunburst employed extreme evasion techniques to avoid detection.
	- It used Sandbox evasions to try and detect if it was running on a virtual machine designed to detect malware and it would stay dormant.
	- It included extensive blacklists which would detect a multitude of forensic tools and AV processes and abort itself if a service was detected that might stop or detect it. The blacklists were disguised as a "Service List" and the hashes of the blacklist items were disguised as "timestamps".
	- It is authored to look completely legitimate even to a skilled eye performing a manual code review. All coding followed Solarwind's codding conventions.
	- The malware was location aware, including blacklists of networks that the software would opt to not run within to further avoid detection.
	- The malware's behavior was also engineered with a time delay and to mimic Solarwind's behavior. This allowed it to fool most dynamic analysis tools.
+ Sunburst made way for additional attacks
	- Once Sunburst determines its threat of detection is low, it levers Command and Control (C2) techniques to dial out to a malicious domain and download a dropper called Teardrop.
+ Teardrop helps attackers map the network, exfiltrate data, and deploy additional tooling to facilitate ongoing access.
	- Teardrop also included advanced evasion techniques including implementation of stenography techniques to hide its malicious traffic within seemingly benign XML.
	- Teardrop only runs in memory (does not install itself), and operates by attaching itself to a Windows Service.
	- Teardrop then drops (i.e. downloads and implements) a payload to further the attackers goals. In some cases it implemented [Cobalt Strike's BEACON](https://www.cobaltstrike.com/help-beacon), which is a widely used pentest tool purpose built to perform advanced attacks.

#### What Have We Learned From Sunburst? ####
+ **Security Tooling Matters:** Sunburst would abort itself if it detected certain types of tooling. Notably EDR and Nextgen AV (like Crowdstrike and SentinelOne), as well as certain network forensics and monitoring tools (reference Appendix A in Check Point Research's article linked below).
+ **SDLC and Change Management Security is an Achilles Heel:** The hackers infiltrated source code, build servers, or both. The attackers went undetected for over a year.
+ **Defense in Depth Matters:** The Sunburst attack was a carefully implemented, phased attack. Any good safeguard along the way may have caused it to abort itself.
+ **All Attacks Ran Disguised as Legitimate Processes or in Memory Only:** This further highlights the fact that traditional AV products are dead. EDR and Nextgen AV is the only way to go.
+ **C2 Infrastructure was Pivotal:** This highlights the additional need for effective classification and segmentation of networks, and ingress/egress rules that limit traffic based on business requirements.
+ **Off the Shelf Pentest Tools Were Used For Harm:** This further highlights the need to control the use of privileged utility programs in the organization, and detect and prevent their usage if not explicitly allowed.

## Further Reading on Sunburst ##
+ [SUNBURST, TEARDROP and the NetSec New Normal](https://research.checkpoint.com/2020/sunburst-teardrop-and-the-netsec-new-normal/), by Check Point Research
+ [FireEye Hack Turns into a Global Supply Chain Attack](https://securityboulevard.com/2020/12/fireeye-hack-turns-into-a-global-supply-chain-attack/), by Security Boulevard
+ [New Evidence Suggests SolarWinds' Codebase Was Hacked to Inject Backdoor](https://thehackernews.com/2020/12/new-evidence-suggests-solarwinds.html), by The Hacker News
