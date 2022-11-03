# Smart Contract Security Verification Standard

## Authors

Damian Rusinek (damian.rusinek@composable-security.com), Paweł Kuryłowicz (pawel.kurylowicz@composable-security.com)

## Introduction

Smart Contract Security Verification Standard (v1.2) is a FREE 14-part checklist created to standardize the security of smart contracts for developers, architects, security reviewers and vendors. This list helps to avoid the majority of known security problems and vulnerabilities by providing guidance at every stage of the development cycle of the smart contracts (from designing to implementation).

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
* [V1: Architecture, Design and Threat Modelling](./0x10-V1-Architecture-Design-Threat-modelling.md)
* [V2: Access Control](./0x11-V2-Access-Control.md)
* [V3: Blockchain Data](./0x12-V3-Blockchain-Data.md)
* [V4: Communications](./0x13-V4-Communications.md)
* [V5: Arithmetic](./0x14-V5-Arithmetic.md)
* [V6: Malicious Input Handling](./0x15-V6-Malicious-Input-Handling.md)
* [V7: Gas Usage & Limitations](./0x16-V7-Gas-Usage-And-Limitations.md)
* [V8: Business Logic](./0x17-V8-Business-Logic.md)
* [V9: Denial of Service](./0x18-V9-Denial-Of-Service.md)
* [V10: Token](./0x19-V10-Token.md)
* [V11: Code Clarity](./0x20-V11-Code-Clarity.md)
* [V12: Test Coverage](./0x21-V12-Test-Coverage.md)
* [V13: Known Attacks](./0x22-V13-Known-Attacks.md)
* [V14: Decentralized Finance](./0x23-V14-Decentralized-Finance.md)

**Severity of the risk**

Threat modelling and risk analysis are important parts of the security assessment. Threat modelling allows to discover the potential threats and their risk impact. The aim of risk analysis is to identify security risks and determine their severity which allows to prioritize them in the mitigation process.

The SCSVS does not include the severity of the risks related to the requirements. Even though there are multiple methodologies to assess the severity, each application is unique and so are the threat actors, their goals, and the impact of a breach. 

Moreover, the requirements cannot be uniquely linked to the security risks as many risks can refer to one requirement and many requirements can refer to one risk.

We recommend to determine the severity of the risks related with the requirements when performing the security assessment using SCSVS standard. 

We recommend [Common Vulnerability Scoring System (CVSS)](https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator), a free and open industry standard for assessing the severity of security vulnerabilities.

**License:**
This work is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License.  To view a copy of this license, visit http://creativecommons.org/licenses/by-sa/4.0/ or send a letter to Creative Commons, PO Box 1866, Mountain View, CA 94042, USA.
