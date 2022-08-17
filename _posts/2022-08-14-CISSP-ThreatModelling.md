---
layout: post
title: "CISSP 2021 - Threat Modelling"
date: 2022-08-14 03:00:00 -0500
categories: [certification]
tags: [certification,cissp,notes]
---

# What is a Threat?

NIST SP 800-30 rev.1

An event that, if it happens, has the potential to impact our ability to operate normally, and does so in a negative way.

# What is Threat Modelling?

Threat modelling is a process by which potential threats, such as structural vulnerabilities, can be identified, enumerated, and prioritized – all from a hypothetical attacker’s point of view.

The threat risk modeling process has five steps:
1. Identify Security Objectives
2. Survey the Application / System
3. Decompose it
4. Identify Threats
5. Identify Vulnerabilities

# Threat Modelling Methodologies

## STRIDE Methodology

Characterizing known threats according to the kinds of exploit that are used (or motivation of the attacker).

|  | Type of Threat | What Was Violated? | How Was It Violated? |
|-------|--------|---------|---------|
| S | Spoofing | Authentication | Impersonating something or someone known and trusted. |
| T | Tampering | Integrity | Modifying data on disk, memory, network, etc. |
| R | Repudiation | Non-repudiation | Claim to not be responsible for an action |
| I | Information Disclosure | Confidentiality | Providing information to someone who is not authorized. |
| D | Denial of Service (DoS) | Availability | Denying or obstructing access to resources required to provide service |
| E | Elevation of Privilege | Authorization | Allowing access to someone without proper authorization |


## DREAD Methodology

Quantifying, comparing and prioritizing the amount of risk presented by each evaluated threat. The DREAD algorithm, shown below, is used to compute a risk value, which is an average of all five categories.

**Risk_DREAD = (DAMAGE + REPRODUCIBILITY + EXPLOITABILITY + AFFECTED USERS + DISCOVERABILITY) / 5**

The calculation always produces a number between 0 and 10; the higher the number, the more serious the risk.

## P.A.S.T.A

Process for Attack Simulation and Threat Analysis (PASTA). A seven-step process for aligning business objectives and technical requirements, taking into account compliance issues and business analysis. Provides a dynamic threat identification, enumeration, and scoring process. Once the threat model is completed security subject matter experts develop a detailed analysis of the identified threats. Finally, appropriate security controls can be enumerated.

Provides an attacker-centric view of the application and infrastructure from which defenders can develop an asset-centric mitigation strategy.

![alt text](/assets/images/threat-modelling/PASTA.png)

## Trike

*Credit to EC-Council for this section*

TRIKE is an open-source threat modeling methodology that is used when security auditing from a risk management perspective. TRIKE threat modeling is a fusion of two models namely – Requirement Model and Implementations Model. The requirement model is the base of TRIKE modeling that explains the security characteristics of an IT system and assigns acceptable levels of risk to each asset. This model also enables coordination among different security teams and stakeholders by providing a conceptual framework. After this comes the implementation model. In this model, a Data Flow Diagram (DFD) is created to illustrate the flow of data and the user performed actions within a system. In this model, threats are analyzed to enumerate and assign a risk value. Based on this, security controls or preventive measures defined to address the threats as per the priority and assigned risks.

![alt text](/assets/images/threat-modelling/TRIKE-Methodology.png)

## VAST

Visual, Agile, and Simple Threat modeling. Focuses on the necessity of scaling the threat modeling process across the infrastructure and entire SDLC, and integrating it seamlessly into an Agile software development methodology. The methodology seeks to provide actionable outputs for the unique needs of various stakeholders: application architects and developers, cybersecurity personnel, and senior executives.

## AS/NZS 4360:2004 Risk Management

the world’s first formal standard for documenting and managing risk.

The five steps of the AS/NZS 4360 process are:
1. Establish Context: Establish the risk domain, i.e., which assets/systems are important?
2. Identify the Risks: Within the risk domain, what specific risks are apparent?
3. Analyze the Risks: Look at the risks and determine if there are any supporting controls in place.
4. Evaluate the Risks: Determine the residual risk.
5. Treat the Risks: Describe the method to treat the risks so that risks selected by the business will be mitigated.

*Note: AS/NZS 4360 assumes that risk will be managed by an operational risk group, and that the organization has adequate skills and risk management resources in house to identify, analyze, and treat the risks.*

