# Smart Contract Security Verification Standard

## Authors

Damian Rusinek, Paweł Kuryłowicz

## Introduction

Smart Contract Security Verification Standard (v1.1) is a FREE 14-part checklist created to standardize the security of smart contracts for developers, architects, security reviewers and vendors. This list helps to avoid the majority of known security problems and vulnerabilities by providing guidance at every stage of the development cycle of the smart contracts (from designing to implementation).

**Objectives**
* Help to develop high quality code of the smart contracts.
* Help to mitigate known vulnerabilities by design.
* Provide a checklist for security reviewers.
* Provide a clear and reliable assessment of how secure a smart contract is in the relation to the percentage of SCSVS coverage.

**Use cases**
You can use the SCSVS checklist in multiple ways:
* As a starting point for formal threat modelling exercise.
* As a measure of your smart contract security and maturity.
* As a scoping document for penetration test or security audit of a smart contract.
* As a formal security requirement list for developers or third parties developing the smart contract for you. 
* As a self-check for developers.
* To point areas which need further development in regards to security.

The entire checklist is in a form similar to OWASP APPLICATION SECURITY VERIFICATION STANDARD v4.0.
Every category has a brief description of the control objectives and a list of security verification requirements.

**Key areas that have been included:**
* V1: Architecture, Design and Threat Modelling
* V2: Access Control
* V3: Blockchain Data
* V4: Communications
* V5: Arithmetic
* V6: Malicious input handling
* V7: Gas Usage & Limitations
* V8: Business Logic
* V9: Denial of Service
* V10: Token
* V11: Code Clarity
* V12: Test Coverage
* V13: Known Attacks
* V14: Decentralized Finance

**Severity of the risk**

Threat modelling and risk analysis are important parts of the security assessment. Threat modelling allows to discover the potential threats and their risk impact. The aim of risk analysis is to identify security risks and determine their severity which allows to prioritize them in the mitigation process.

The SCSVS does not include the severity of the risks related to the requirements. Even though here exist multiple methodologies to assess the severity, each application is unique and so are the threat actors, their goals, and the impact of any breach. 

Moreover, the requirements cannot be uniquely linked to the security risks as many risks can refer to one requirement and many requirements can refer to one risk.

We recommend to determine the severity of the risks related with the requirements when performing the security assessment using SCSVS standard. 

We recommend [Common Vulnerability Scoring System (CVSS)](https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator), a free and open industry standard for assessing the severity of security vulnerabilities.

**License:**
This work is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License.  To view a copy of this license, visit http://creativecommons.org/licenses/by-sa/4.0/ or send a letter to Creative Commons, PO Box 1866, Mountain View, CA 94042, USA.
