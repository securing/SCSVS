# V3: Blockchain data

## Control Objective

[Description]

Category “V3” lists requirements related to the blockchain data of the smart contracts.

## Security Verification Requirements

| # | Description | Since |
| --- | --- | --- |
| **1.1** | Verify that visibility of all functions is specified. | 1.0 |
| **1.2** | Do not assume that any data saved in blockchain is safe and private. | 1.0 |
| **1.3** | Verify that the list of sensitive data processed by the smart contract is identified, and that there is an explicit policy for how access to this data must be controlled, encrypted and enforced under relevant data protection directives. | 1.0 |
| **1.4** | Do not use string literals as keys for mappings. Use global constants instead to prevent homoglyphs attacks. | 1.0 |


## References

For more information, see also:

* [Homoglyph attack](https://github.com/Arachnid/uscc/tree/master/submissions-2017/marcogiglio)
* [OWASP Attack Surface Analysis Cheat Sheet](https://www.owasp.org/index.php/Attack_Surface_Analysis_Cheat_Sheet)
* [OWASP Threat modeling](https://www.owasp.org/index.php/Application_Threat_Modeling)
* [OWASP Secure SDLC Cheat Sheet](https://www.owasp.org/index.php/Secure_SDLC_Cheat_Sheet)
* [Microsoft SDL](https://www.microsoft.com/en-us/sdl/)
* [NIST SP 800-57](https://csrc.nist.gov/publications/detail/sp/800-57-part-1/rev-4/final)