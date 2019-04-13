# V1: Architecture, design and threat modelling

## Control Objective

Ensure that a verified contract satisfies the following high level requirements:
* TODO

Category “V1” lists requirements related to the architecture, design and threat modelling of the smart contracts.

## Security Verification Requirements

| # | Description | Since |
| --- | --- | --- |
| **1.1** | Verify the use of threat modeling for every design change or sprint planning to identify threats, plan for countermeasures, facilitate appropriate risk responses, and guide security testing. | 1.0 |
| **1.2** | Verify documentation and justification of all the contract trust boundaries (trusted relations with other contracts and significant data flows).  | 1.0 |
| **1.3** | Verify availability of a secure coding checklist, security requirements, guideline, or policy to all developers and testers. | 1.0 |
| **1.4** | Verify that there exists an upgrade mechanism for contract which allows to deploy the security fixes. | 1.0 |
| **1.5** | Verify that there is a component that monitors contract activity using events. | 1.0 |
| **1.6** | Verify that there exists a mechanism that can temporary stop the sensitive functionalities of the contract in case of a new attack. This mechanism should not block access to the assets (e.g. tokens) for the owners. | 1.0 |
| **1.7** | Verify that there is a policy to track new security bugs and to update the libraries to the latest stable version. | 1.0 |
| **1.8** | Verify that the amount of cryptocurrencies kept on contract is controlled and at the minimal acceptable level. | 1.0 |
| **1.9** | Verify that if fallback function can be called by anyone it is included in the threat modelling. | 1.0 |
| **1.10** | Verify that the business logic in contracts is consistent. Important changes in the logic (e.g. upgradeability) should be allowed for all or none contract. | 1.0 |
| **1.11** | Verify that a code analysis tools is in use that can detect potentially malicious code. | 1.0 |
| **1.12** | Verify that the latest version of solidity is used. | 1.0 |

## References

For more information, see also:

* [OWASP Threat Modeling Cheat Sheet](https://www.owasp.org/index.php/Threat_Modeling_Cheat_Sheet)
* [OWASP Attack Surface Analysis Cheat Sheet](https://www.owasp.org/index.php/Attack_Surface_Analysis_Cheat_Sheet)
* [OWASP Threat modeling](https://www.owasp.org/index.php/Application_Threat_Modeling)
* [OWASP Secure SDLC Cheat Sheet](https://www.owasp.org/index.php/Secure_SDLC_Cheat_Sheet)
* [Microsoft SDL](https://www.microsoft.com/en-us/sdl/)
* [NIST SP 800-57](https://csrc.nist.gov/publications/detail/sp/800-57-part-1/rev-4/final)