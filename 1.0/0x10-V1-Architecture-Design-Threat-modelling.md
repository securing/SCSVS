# V1: Architecture, design and threat modelling

## Control Objective

Architecture, design and threat modelling in the context of creating secure smart contracts.
Consider all possible threats before the implementation of the smart contract.

Ensure that a verified contract satisfies the following high level requirements:
* All related smart contracts are identified and used properly,
* Specific smart contracts security assumptions are considered during the design phase.

Category “V1” lists requirements related to the architecture, design and threat modelling of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **1.1** | Verify that every introduced design change is preceded by an earlier threat modelling. | 
| **1.2** | Verify that the documentation clearly and precisely defines all trust boundaries in the contract (trusted relations with other contracts and significant data flows).  | 
| **1.3** | Verify that SCSVS, security requirements or policy is available to all developers and testers. | 
| **1.4** | Verify that there exists an upgrade mechanism for contract which allows to deploy the security fixes. | 
| **1.5** | Verify that there is a component that monitors contract activity using events. | 
| **1.6** | Verify that there exists a mechanism that can temporarily stop the sensitive functionalities of the contract in case of a new attack. This mechanism should not block access to the assets (e.g. tokens) for the owners. | 
| **1.7** | Verify that there is a policy to track new security bugs and to update the libraries to the latest secure version. | 
| **1.8** | Verify that the amount of cryptocurrencies kept on contract is controlled and at the minimal acceptable level. | 
| **1.9** | Verify that if fallback function can be called by anyone it is included in the threat modelling. | 
| **1.10** | Verify that the business logic in contracts is consistent. Important changes in the logic (e.g. upgradeability) should be allowed for all or none contract. | 
| **1.11** | Verify that code analysis tools are in use that can detect potentially malicious code. | 
| **1.12** | Verify that the latest version of solidity is used. | 

## References

For more information, see also:
* [OWASP Threat Modeling Cheat Sheet](https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/Threat_Modeling_Cheat_Sheet.md)
* [OWASP Attack Surface Analysis Cheat Sheet](https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/Attack_Surface_Analysis_Cheat_Sheet.md)
* [OWASP Threat modeling](https://www.owasp.org/index.php/Application_Threat_Modeling)
* [Microsoft SDL](https://www.microsoft.com/en-us/sdl/)
* [NIST SP 800-57](https://csrc.nist.gov/publications/detail/sp/800-57-part-1/rev-4/final)