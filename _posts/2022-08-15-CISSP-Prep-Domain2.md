---
layout: post
title: "CISSP 2021 Prep Notes - Domain 2 - Asset Security"
date: 2022-08-15 10:00:00 -0500
categories: [certification]
tags: [certification,cissp,notes]
---

*** These are my compiled notes from the Accelerated CISSP (2021) course put on by ITProTV ***

# CISSP Domain 2 - Asset Security

## Key Points

1. Classification and Categorization
    * Data owners are responsible for classifying data, making sure it is labelled in such a way that only authorized subjects are able to interact with it.
    * The value that data has as an asset to the organization, ensuring that if the data became inaccessible for any reason, that we understand the impact of the loss; allows us to assign value upfront and apply appropriate controls and countermeasures 
2. How to manage sensitive information
    * importance of asset labelling; everyone should know what classification of data is on the media
3. Data/retention policies
    * help us understand the lifecycle and scope of the data
4. Data policy
    * how to govern and manage data
5. Asset Inventory | Classification | Labeling | Handling

6. Data Classification Schemes (2 types - Government and Private Sector)
    1. Government
        1. Top Secret
        2. Secret
        3. Confidential
        4. Unclassified
    2. Private Sector
        1. Confidential
        2. Private
        3. Sensitive
        4. Public

7. NIST NICE Framework: Securely Provision (SP) NICE Specialty Areas
    1. Risk Management (RSK)
    2. Software Development (DEV)
    3. Systems Architecture (ARC)
    4. Technology R&D (TRD)
    5. Systems Requirements Planning (SRP)
    6. Test & Evaluation (TST)
    7. Systems Development (SYS)

8. Data Lifecycle Management (DLM) vs. Information Lifecycle Management (ILM)
    1. Data Management Lifecycle (PLAN + 5 Phases)
        0. PLAN FIRST!!
        1. Data Creation
        2. Storage
        3. Usage/Share
        4. Archival
        5. Destruction
    2. ILM is focused on the accuracy of the data
    3. DLM focusses on the lifecycle of the data overall

9. QA (external) vs. QC (internal) & Collection Limitation on data
    * QA makes sure we align with external standards and regulations to prove that we are building and doing things in an appropriate fashion
    * QC focusses on standards driven internally by the organization and making sure we are meeting internal quality goals
    * Collection limitations, particularly around PII and PHI; cannot use data outside what has been communicated and agreed to with the data subject

10. Roles to know:
    1. Data Subject - subject of personal data
    2. Data Owner - master of all
    3. Data Controller - determines processing purpose(s)
    4. Data Processor - managers of all (on behalf of the controller)
    5. Data Custodian - custody, transport, storage & business rules
    6. Data Steward - fitness of data elements; integrity and accuracy
    7. Administrator - grants permissions / access to data

11. Data, data, data - Remanence & Sanitization
    1. Clearing - basic built-in tools; formatting; cleaning the surface (used when recycling the media for use in the same classification zone)
    2. Purging - multi-overwriting; low-level formatting
    3. Destruction
        1. Overwriting
        2. Degaussing
        3. Encryption
        4. Crypto-Shredding or Crypto-Sharding
            * encrypting data, re-encrypting it, separating the data from the key, and destroying
            * used in cloud environments when you do not actually have access to the data
        5. Physical Destruction
        6. Chemical ALteration
        7. Phase Shift/transition (Curie Temp)
        * ** SSD and HDD cannot be handled the same way; SSD cannot simply format, must use built-in vendor tools i.e. Secure Erase
    4. Simple Delete = Erase
    * ** Cloud data - encrypt data while in storage and use ==> upon exit crypto-shred remaining data

12. Asset Retention - What are the stages?
    1. GA/Sale Date
    2. End of Life/End of Sale
    3. End of Development
    4. End of Service Life/End of Support

13. End-of-Life Management
    1. Maintaining inventories
    2. Approved end-of-life or sunset policy
    3. Tracking changes, availability of updates, and end of support
    4. Risk assessments to determine end-of-life; may need to keep an asset around after vendor EoL given business requirements and risk appetite
    5. Plan for the replacement of systems and comply with policy requirements
    6. Procedures for secure destruction or data wiping of hard drives

14. Data States
    * ** Data exists in 3 well defined states:
    1. At Rest (Storage)
    2. In Motion (Transmit/on the wire)
    3. In Use (Application in Memory)

15. Link vs. End-to-End Encryption
    * Link encryption secures all elements of the data package
    * End-to-End encryption only secures the data payload/message

16. Scoping & Tailoring (Supplementation)
    * Scoping is about what is covered and what is excluded
    * Tailoring is how we modify and customize the scope to make a one-size-fits-one solution
    * Supplementation is used to add in and bring additional things that allow us to create an exact solution to what is needed
    * Allow us to determine what controls are required and how to best apply them to deal with risk

17. Standards...
    * ISO
    * NIST
    * CIS Controls
        * Basic
        * Foundational
        * Organizational
    * NIST SCAP (Security Content Automation Protocol)
        * Assessment platform that helps us understand the current state of our systems, looking for gaps or weaknesses, and identifying them for remediation

18. Data Protection Methods (Digital Rights Management (DRM), Data Loss Prevention (DLP), Cloud Access Security Broker (CASB))
    * At Rest (Storage)
        1. Encryption
        2. Obfuscation/Tokenization
        3. Archive/Disposal/Destruction
        4. Mobile Device Protection
        5. Physical Media Control
    * In Motion (Transit)
        1. Encryption
        2. Perimeter Security
        3. Web Content Filtering
        4. NEtwork Traffic Monitoring
        5. VPN's
    * In Use (Application)
        1. Encryption
        2. User Monitoring
        3. Workstation Restrictions
        4. Application Controls (whitelist/blacklist)
        5. Data Labeling