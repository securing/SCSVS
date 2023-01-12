# Smart Contract Security Verification Standard  🚀

## Authors

* Damian Rusinek [@drdr_zz](https://twitter.com/drdr_zz) (damian.rusinek@composable-security.com)
* Paweł Kuryłowicz [@wh01s7](https://twitter.com/wh01s7) (pawel.kurylowicz@composable-security.com)

## Introduction

Smart Contract Security Verification Standard (v2) is a FREE checklist created to **standardize the security of smart contracts** for developers, architects, security reviewers, and vendors. 

This list helps to avoid the majority of known security problems and vulnerabilities by guiding at every stage of the development cycle of smart contracts (from design to implementation).

**Objectives**
* Help to develop high-quality code of smart contracts.
* Help to mitigate known vulnerabilities by design.
* Provide a checklist for security reviewers.
* Provide a clear and reliable assessment - **Security Health Factor** - of how secure smart contracts are in the relation to the percentage of SCSVS coverage.

## 🔥 Updates in v2 🔥

Security, Composability, and Transparency are fundamentals of the SCSVS. These values are achieved thanks to the engagement and cooperation of the #BlockSec community. The standard structure distinguishes 3 chapters, each operating in a slightly different area.

* **General** - common and general security problems including, among others: design, upgrades, and policies.
* **Components** - contracts that make up the project, frequently used patterns with their typical security issues.
* **Integrations** - components with which the project integrates, general recommendations and threats to frequently used smart contracts.

## How to use SCSVSv2

You can use the SCSVS checklist in multiple ways:
* As a starting point for formal threat modeling exercise.
* As a measure of your smart contract security and maturity.
* As a scoping document for a penetration test or security audit of a smart contract.
* As a formal security requirement list for developers or third parties developing the smart contract for you. 
* As a self-check for developers.
* To point out areas that need further development regarding security.

Depending on your role in the protocol, we recommend performing different actions summarized below. Treat it as an inspiration and not strict rules.

### As Architect 👷‍♂️

If you are designing a protocol, you should schedule (and potentially delegate) the following actions:
* Use security requirements from the General and Components chapters to identify potential security bugs your team might introduce in the protocol.
* Use security requirements from the Interaction chapter to identify potential threats coming from the 3rd party protocols.
* Write down all potential threats identified in steps 1 and 2. This will be great input for the threat modeling session.
* Inform your team about the identified threats (e.g. during a threat modeling session).

### As Developer 🧑‍💻

If you are developing a protocol, you should schedule (and potentially delegate) the following actions:
* Get the potential threats identified by the Auditor, Architect or during a threat modeling session and learn how to avoid them.
* When implementing a smart contract with specific functionalities, check the security requirements from the corresponding SCSVS category.
* After release, make sure the SCSVS coverage report is present in the protocol repository.

### As Business Owner / Founder 🧙

If you are the owner of a protocol or represent the business side of the project, you should schedule and delegate the following actions:
* Ask other protocols teams that yours is integrated with for their SCSVS coverage report.
* Check the **Security Health Factor** of your protocol by doing SCSVS coverage of all 3 chapters.

### As Auditor 🥷

If you are an internal or external auditor of a protocol, you should schedule (and potentially delegate) the following actions:
* Do a threat modeling session (as soon as possible) to identify potential threats and decide how to handle them. Use the output of Architect actions as partial input.
* Just before the release, do the SCSVS coverage of all 3 chapters to get the **Security Health Factor** of your protocol.
* Add SCSVS coverage report to the protocol repository.

## Table of contents

* G: General
    * [G1: Architecture, design and threat modeling](<./2.0/0x100-General/0x101-G1-Architecture-Design-Threat-Modeling.md>)
    * [G2: Policies and procedures
](<./2.0/0x100-General/0x102-G2-Policies-procedures.md>)
    * [G3: Upgradeability](<./2.0/0x100-General/0x103-G3-Upgradeability.md>)
    * [G4: Business logic](<./2.0/0x100-General/0x104-G4-Business-Logic.md>)
    * [G5: Access control](<./2.0/0x100-General/0x105-G5-Access-Control.md>)
    * [G6: Communications](<./2.0/0x100-General/0x106-G6-Communications.md>)
    * [G7: Arithmetic](<./2.0/0x100-General/0x107-G7-Arithmetic.md>)
    * [G8: Denial of service](<./2.0/0x100-General/0x108-G8-Denial-of-Service.md>)
    * [G9: Blockchain data](<./2.0/0x100-General/0x109-G9-Blockchain-Data.md>)
    * [G10: Gas usage & limitations](<./2.0/0x100-General/0x110-G10-Gas.md>)
    * [G11: Code clarity](<./2.0/0x100-General/0x111-G11-Code-Clarity.md>)
    * [G12: Test coverage](<./2.0/0x100-General/0x112-G12-Test-Coverage.md>)
* C: Components
    * [C1: Token](<./2.0/0x200-Components/0x201-C1-Token.md>)
    * [C2: Governance](<./2.0/0x200-Components/0x202-C2-Governance.md>)
    * [C3: Oracle](<./2.0/0x200-Components/0x203-C3-Oracle.md>)
    * [C4: Vault](<./2.0/0x200-Components/0x204-C4-Vault.md>)
    * [C5: Bridge](<./2.0/0x200-Components/0x205-C5-Bridge.md>)
* I: Integrations
    * [I1: Basic](<./2.0/0x300-Integrations/0x301-I1-Basic.md>)
    * [I2: Token](<./2.0/0x300-Integrations/0x302-I2-Token.md>)
    * [I3: Oracle](<./2.0/0x300-Integrations/0x303-I3-Oracle.md>)

## Severity of the risk

Threat modeling and risk analysis are important parts of the security assessment. Threat modeling allows the discovery of potential threats and their risk impact. Risk analysis aims to identify security risks and determine their severity, which allows the team to prioritize them in the mitigation process.

The SCSVS does not include the severity of the risks related to the requirements. Even though there are multiple methodologies to assess the severity, each application is unique and so are the threat actors, their goals, and the impact of a breach. 

Moreover, the requirements cannot be uniquely linked to the security risks, as many risks can refer to one requirement and many requirements can refer to one risk.

We recommend determining the severity of the risks related to the requirements when performing the security assessment using the SCSVS standard. 

We recommend [Common Vulnerability Scoring System (CVSS)](https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator), a free and open industry standard for assessing the severity of security vulnerabilities.

## License
This work is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License.  To view a copy of this license, visit http://creativecommons.org/licenses/by-sa/4.0/ or send a letter to Creative Commons, PO Box 1866, Mountain View, CA 94042, USA.

The entire checklist is in a form similar to OWASP APPLICATION SECURITY VERIFICATION STANDARD v4.0.
Every category has a brief description of the control objectives and a list of security verification requirements.
