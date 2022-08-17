---
layout: post
title: "CISSP 2021 Prep Notes - Domain 1 - Security and Risk Management"
date: 2022-08-14 10:00:00 -0500
categories: [certification]
tags: [certification,cissp,notes]
---

*** These are my compiled notes from the Accelerated CISSP (2021) course put on by ITProTV ***

# CISSP Domain 1 - Security and Risk Management

## Key Points

1. Code of Ethics!!
    * Protect society, the common good, necessary public trust and confidence, and the infrastructure.
    * Act honorably, honestly, justly, responsibly, and legally.
    * Provide diligent and competent service to principals.
    * Advance and protect the profession.
2. CIA Triad
    * Confidentiality - keep good data away from bad people
        * Countermeasures:
            * encryption
            * traffic padding
            * strict access controls / authentication
            * data classification
            * awareness training
    * Integrity - can't change data without knowledge and consent of the owner
        * Countermeasures:
            * strict access controls / authentication
            * IDS
            * encryption
            * hashing
            * interface restrictions / controls
            * input / function checks (validation)
    * Availability - making sure authorized users can access data
        * Countermeasures:
            * strict access controls / authentication
            * continuous monitoring
            * firewalls & routers to prevent DoS / DDoS attacks
            * redundant system design
            * periodic testing of backup systems
3. What is Governance?
    * Information security management validates appropriate policies, procedures, standards, and guidelines are implemented to ensure business operations are conducted within an acceptable level of risk.
    * A Security Framework
        * acts as a reference point
        * provides a common language for communications (CULTURE OF SECURITY)
        * allows us to share information and create relevancy
    * Governance – how an organization is managed; providing oversight to the activities of an organization
    * Security Governance – how security is managed, through policies, roles, and processes used to make security decisions.
    * Governance Committee – a formal decision making body within the organization.
    * Note:
        * Security must align with organizational goals (not dominate or drive them).
    * Due Diligence - making sure we are doing what we need to do; oversight and governence
    * Due Care - acting in appropriate ways that align with business requirements
    
4. SABSA, TOGAF, & Zachman
    * [SABSA, TOGAF, and Zachman]({% post_url 2022-08-14-CISSP-Prep-Frameworks %})
    * ISO 27001 - ISMS
    * ISO 27002 - controls that should be applied to flesh out ISMS architecture
    * ISO 31000 - default standard for Risk Management
    * ISO 15408 - Common Criteria for Information Technology Security Evaluation
    * NIST SP 800-30 rev.1 - vocabulary of risk
    * NIST SP 800-37 rev.2 - Risk Management Framework
    * NIST SP 800-161 - Supply chain risk
    * COBIT - framework for documenting IT risk
        
5. Privacy, PII, PHI, & GDPR
6. Cyber Crimes and Data Breaches
    * When assessing the effect of cybercrime, you need to evaluate areas such as:
        * Loss of intellectual property and / or sensitive data
        * Damage to brand image/reputation
        * Penalties and compensatory payments
        * Cost of countermeasures
6. Intellectual Property - [see here]({% post_url 2022-08-14-CISSP-Prep-IntellectualProperty %})
7. The 8 Core Principles (OECD)
    1. Collection Limitation
    2. Data Quality
    3. Purpose Specification
    4. Use Limitation
    5. Security Safeguards
    6. Openness
    7. Individual Participation
    8. Data Controller Accountability
8. GDPR - [see here]({% post_url 2022-08-14-CISSP-GDPR %})
9. Different Types of Investigations:
    * Administrative - INTERNAL
    * Criminal - conducted by law enforcement
    * Civil - present a case in a civil trial
    * Regulatory - government agency
    * Industry standards - Electronic Discovery (eDiscovery) used to facilitate the processing of electronic information for disclosure
10. Identify, Analyze, and Prioritize Business Continuity Requirements
    1. Develop and document scope and plan
        * Project Management
        * Senior Management Support
        * Project Scope
        * Resources
        * Timeline
    2. Business Impact Analysis (BIA)
        * Used to determine what impact a disruptive event would have on an organization
        * Goals:
            1. Determine Criticality
            2. Estimate Maximum Downtime
            3. Evaluate Internal and External Resource Requirements
    3. Process Steps:
        1. Gather requirements/information
        2. Vulnerability assessment
        3. Quantitative Risk Analysis
            * ALE = SLE * ARO ===> ALE = (AV*EF) * ARO
                * Exposure Factor (EF) - % of loss experienced IF a specific asset were attacked
                * Single Loss Expectancy (SLE) - the cost associated with a single realized risk against a single asset
                    *  SLE = AV * EF 
                    * (Single Loss Expectancy) = (Asset Value) * (Exposure Factor %)
                * Annualized Rate of Occurrence (ARO) - frequency at which a specified risk will be realized over a single year
                * Annualized Loss Expectancy (ALE) - potential yearly cost of all instances of a specified threat
                * Asset Value (AV) - $$$ amount asset is worth to the organization
            * If control cost is less than ALE, implement control
            * If control cost is equal to ALE, implement control
            * If control cost is greater than ALE, look at qualitative aspects
        4. Communicate findings - Audience relevancy
    4. Determining Downtime:
        * Maximum Allowable Downtime (MAD) / Maximum Tolerable Downtime (MTD)
            * Maximum amount of time the system can be offline before bad things happen
            * MTD = RTO + WRT
        * Recovery Time Objective (RTO)
            * Minimum specified amount of time it should take to bring systems back online
        * Work Recovery Time (WRT)
            * Additional time it takes to validate recovered data and ensure integrity of recovered data
        * Recovery Point Objective (RPO)
            * Amount of data we stand to lose during a recovery event
        * ![alt text](/assets/images/business-continuity/mtd-diagram.png)
11. Threat Modelling - [see here]({% post_url 2022-08-14-CISSP-ThreatModelling %})
12. Supply Chain Risk Management
    1. Risks associated with hardware, software, and services
        * *NIST SP800-161 - Supply Chain Risk Management Practices for Federal Information Systems and Organizations (page 7)*
        * Supply chain risks include insertion of counterfeits, unauthorized production, tampering, theft, insertion of malicious software and hardware (e.g., GPS tracking devices, computer chips, etc.), as well as poor manufacturing and development practices in the supply chain. These risks are realized when threats in the supply chain exploit existing vulnerabilities.
    2. Third-party assessment and monitoring
        * SLA's vs. Assurance via Due Diligence
        * Holding a vendor to a verifiable standard
    3. Minimum security requirements
        * Requirements Gathering
    4. Service-level requirements
        * SLA vs SLR
        * SLR's make up an SLA
    5. Onsite Assessment, Document Exchange and Review Process/Policy Review, Third Party Audit
    6. Managing known risks
        1. Identify and document risks
        2. Build a supply-chain risk-management framework
        3. Monitor risk
        4. Institute governance and regular review
    7. Supply Chain Risk Management Strategies
        1. PPRR risk management model - a popular global supply chain risk management strategy and is used by retailers around the world. “PPRR” stands for:
            * Prevention - Take precautionary measures for supply chain risk mitigation.
            * Preparedness - Develop and implement a contingency plan in case of an emergency.
            * Response - Execute on your contingency plan in order to reduce the impact of the disruptive event.
            * Recovery - Resume operations and get things running at normal capacity as quickly as possible.
        2. Manage environmental risk in your supply chain - single vs. multi supplier
    8. Supply chain risk assessment software enables you to take a proactive approach to risk management by providing you with greater visibility into the structure of your supply chain. With such a solution, you will be able to identify weak points in your supply chain and receive data-driven insights into how you can strengthen them.
    9. Improve your cyber supply chain risk management:
        * Establish compliance standards for all third-party vendors, including manufacturers, suppliers, and distributors.
        * Define user roles and implement security controls to restrict who is able to access your system and what level of clearance they are given.
        * Perform a thorough vendor risk assessment prior to signing any contracts.
        * Implement data stewardship standards that define who owns certain data and what they are able to do with that data.
        * Provide comprehensive training for all employees about cybersecurity protocols.
        * Implement a software solution that provides you with total visibility into your supply chain, so you can quickly identify unusual activity.
        * Work with vendors in your supply chain network to develop a unified disaster recovery plan to ensure business continuity.
        * Establish backup controls to safeguard your data backups.
        * Regularly update your company’s anti-virus, anti-spyware, and firewall software solutions, as well as look into more advanced cybersecurity measures, such as DNS filtering and network access control.
    10. Gain visibility into suppliers’ financial stability
    11. Track the right freight carrier metrics:
        * Transit Time - the number of hours or days it takes for a shipment to arrive at the customer’s location after leaving your facility.
        * Number of Stops & Average Stop Time - The more stops a freight carrier takes in route to delivering a shipment, the longer it will take your product to reach your customer. Even if a route only includes a few stops, a long average stop time could still jeopardize on-time delivery and disrupt your supply chain. These metrics are important to monitor for the sake of supply chain efficiency.
        * *[Note: It’s important to look for a low number of stops and low average stop time while still being mindful of drivers’ legally regulated hours of service.]*
        * Average Loading Time - This refers to the amount of time it takes to load a carrier with freight, as well as fill out any necessary paperwork, once it has arrived at the loading dock. Like the previous item on this list, this is a key indicator of supply chain efficiency.
        * Route Optimization - It’s important that retailers consider how field carriers optimize routes for fuel usage and travel time because these have a direct effect on supply chain costs and efficiency. If a retailer has its own fleet, it can monitor this metric closely; if it partners with a third-party carrier, it can monitor this metric through costs charged for shipping.
        * Maintenance Schedule - A freight carrier with a consistent maintenance schedule is less likely to break down, which can prevent unnecessary supply chain disruption.
    12. Implement a logistics contingency plan - Similar to an emergency response plan, it’s imperative that retailers have a logistics contingency plan in place to ensure business continuity in the event of supply chain disruption.
        * Some tips when creating a contingency plan for supply chain risk mitigation:
            * Map out your supply chain to get a clear understanding of which entities are most vulnerable to risk.
            * Perform a full assessment of suppliers based on factors such as political risk, geographic risk, and economic risk.
            * Diversify your supplier network so that you are not reliant on a single supplier.
            * Audit logistics providers based on their disaster plans.
            * Establish a crisis response team to make critical decisions in the event of an emergency.
            * Develop solid communications channels so that your employees know what their responsibilities are in the event of supply chain disruption.
            * Carefully document all processes and create a single source of truth that employees can refer to when executing on your contingency plan.
            * Stay up to date on current events and adapt your contingency plan accordingly.
    13. Conduct internal risk awareness training - Management is not the only area of your organization that can assist in supply chain risk mitigation. In fact, building a risk-aware culture requires buy-in at all levels of your business. The easiest way to achieve this is to conduct risk awareness training for your entire workforce. Training curriculum should include the following:
        * Common supply chain management risks and challenges
        * Risk management best practices
        * Computer and internet best practices to improve cybersecurity awareness
        * Supply chain risk assessment software training to encourage end user adoption
    14. Consistently monitor risk
    15. Use data to model key risk event scenarios
    16. Consolidate your data for easy access
13. Security Awareness Education & Training Program
    * Establishing an understanding of the importance of, and need to, comply with security policies within the organization
    * Addresses the "WHY" of policy:
    * Methods and techniques to present awareness and training
    * Periodic content reviews
    * Program effectiveness evaluation
        * Program means nothing if it does not prove its effectiveness