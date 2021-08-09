---
layout: 	post
title:  	DevOps and DevSecOps Overview
subtitle: 	Tuesday Morning Grind, Ep 7
date:   	2020-12-08
author: 	Shane Peden
header-img: img/blueheader.jpg
catalog: 	true
tags:
    - SDLC
    - Podcast
    - ITAudit
    - DevOps
---

> Tuesday Morning Grind, Ep 7 - DevOps and DevSecOps Overview

<iframe width="560" height="315" src="https://www.youtube.com/embed/uz0Zk_il3l0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Podcast Summary
IT Auditors and Security Assessors often have a hard time understanding the risks associated with the modern software engineering ecosystem. In this episode we discuss DevOps and DevSecOps, potential risks security assessors should understand, and common tool sets that support these approaches to engineering.

## DevOps and DevSecOps Overview

#### What is DevOps? ####
+ DevOps brought together the traditionally siloed world of software engineering and IT operations
	- The skill-sets of the modern IT practitioner have changed drastically over the past decade. 
	- Skill-sets for modern IT practitioners have a lot more overlap with software engineers.
	- In DevOps we see a paradigm shift in how software is delivered and supported. A continuous feedback loop keeps development and infrastructure teams marry the software engineering and infrastructure management teams. 

+ Many information security frameworks attempt to over simplify change management and the SDLC.
	- Oftentimes view the world from a more traditional Waterfall methodology approach.
	- Assumes processes are linear and sequential. 
	- To outsiders, software development teams may appear to have a lack of control over their SDLC.
		
#### DevOps Tool-chain ####
+ Tooling is critical to defining the style, workflow, and culture of a DevOps team. 
	- DevOps would not be possible without the modern cloud.
	- Specialized tools exist at every phase of the life-cycle to enable the process. These tools are almost always designed to integrate with other tools to the left or right of it in the DevOps life-cycle. 
+ The security assessor and IT auditor should be able to identify risk throughout the life-cycle. For example: 
	- Change management and oversight is taking place throughout, but starts as tickets in the Plan and Code phase.
	- Control over source code is a concern in the Plan and Code, and Build phases.
	- QA and various forms of testing should be assessed throughout the build, Test and Release, and Deployment phases.
	- Rollback plans should be developed and in place as part of the Deploy phase.
	- External security assessments and availability monitoring should be in place within the Operate and Monitor phase.
	
#### DevSevOps Tool-chain ####
+ DevSecOps is the integration of security into the DevOps life-cycle.
	- Security integration should be as systematic and automated as possible. 
	- DevSecOps is a risk based strategy. Teams will have to determine the opportunity cost of every security integration they choose (or choose not) to implement. 
	- I have authored an in-depth whitepaper which discusses multiple approaches to integrating security throughout the DevOps life-cycle. Request it here: [risk3sixty DevSecOps Whitepaper](https://risk3sixty.com/whitepaper/devsecops-strategies-to-achieve-security-by-design/)

#### Key Concepts of DevOps ####
+ Agile methodology helps us break down large bodies of work into manageable tasks.
+ Continuous integration and delivery/deployment are key to automating the merging, testing, and deployment functions for software releases.
+ Source code repositories (nearly always Git) enable automation and version control capabilities which are foundational to DevOps.
+ IT Service Management and Site Reliability Engineering is the evolution of delivering IT services as a service. It is an integration of many development technologies and approaches to delivering IT services.
+ Incident Management is the organization’s ability to handle unplanned changes, bugs, vulnerabilities, and service interruptions. 

#### What is next in the series? ####
- Part 1: [DevOps and DevSecOps Overview](https://r3s-shane.github.io/2020/12/01/tmg-episode-6/)
- Part 3: [How to Effectively Audit the DevOps SDLC](https://r3s-shane.github.io/2020/12/15/tmg-episode-8/)

### More About The Tuesday Morning Grind
The Tuesday Morning Grind is a podcast I do every Tuesday at 7am with my teammate, [Christian Hyatt](https://www.linkedin.com/in/christianhyatt/).  You can watch the live-stream on [Twitch](https://www.twitch.tv/risk3sixty), catch the video later on [Youtube](https://www.youtube.com/channel/UCjcD3Vc3Z1FSncd2BvRp9vQ/featured) or subscribe on your platform of choice over at [Anchor FM](https://anchor.fm/risk3sixty).



