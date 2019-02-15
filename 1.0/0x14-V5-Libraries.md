# V5: Libraries

## Control Objective

[Description]

Category “V5” lists requirements related to the libraries of the smart contracts.

## Security Verification Requirements

| # | Description | Since |
| --- | --- | --- |
| **1.1** | Use the approve function of the ERC-20 standard to change allowed amount only to 0 or from 0. | 1.0 |
| **1.2** | Verify that you do not rely the contract logic on the balance of contract (eg. balance == 0). | 1.0 |
| **1.3** | Verify libraries that are not part of the application but that the smart contract relies on to operate are identified. | 1.0 |
| **1.4** | Verify libraries that call external security services have a centralized implementation. | 1.0 |
| **1.5** | Verify that there is a centralized mechanism for protecting access to each type of protected resource. | 1.0 |
| **1.6** | Verify that sensitive data is rapidly sanitized from memory as soon as it is no longer needed and handled in accordance to functions and techniques supported by the library. | 1.0 |
| **1.7** | Make sure that used libraries are up to date. |1.0 |
| **1.8** | Make sure all library functions that should be upgradeable are not internal. |1.0 |


## References

For more information, see also:

* [OWASP Threat Modeling Cheat Sheet](https://www.owasp.org/index.php/Threat_Modeling_Cheat_Sheet)
* [OWASP Attack Surface Analysis Cheat Sheet](https://www.owasp.org/index.php/Attack_Surface_Analysis_Cheat_Sheet)
* [OWASP Threat modeling](https://www.owasp.org/index.php/Application_Threat_Modeling)
* [OWASP Secure SDLC Cheat Sheet](https://www.owasp.org/index.php/Secure_SDLC_Cheat_Sheet)
* [Microsoft SDL](https://www.microsoft.com/en-us/sdl/)
* [NIST SP 800-57](https://csrc.nist.gov/publications/detail/sp/800-57-part-1/rev-4/final)