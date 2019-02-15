# V4: Arithmetic

## Control Objective

[Description]

Category “V4” lists requirements related to the arithmetic of the smart contracts.

## Security Verification Requirements

| # | Description |  Since |
| --- | --- | --- | 
| **1.1** | Use SafeMath for arithmetic operations. | 1.0 |
| **1.2** | Make sure the values are resistant to integer overflows. | 1.0 |
| **1.3** | Verify that you do not rely the contract logic on the balance of contract (eg. balance == 0). | 1.0 |
| **1.4** | Verify that non-strict inequality is used for balance equality. | 1.0 |


## References

For more information, see also:

* [OWASP Threat Modeling Cheat Sheet](https://www.owasp.org/index.php/Threat_Modeling_Cheat_Sheet)
* [OWASP Attack Surface Analysis Cheat Sheet](https://www.owasp.org/index.php/Attack_Surface_Analysis_Cheat_Sheet)
* [OWASP Threat modeling](https://www.owasp.org/index.php/Application_Threat_Modeling)
* [OWASP Secure SDLC Cheat Sheet](https://www.owasp.org/index.php/Secure_SDLC_Cheat_Sheet)
* [Microsoft SDL](https://www.microsoft.com/en-us/sdl/)
* [NIST SP 800-57](https://csrc.nist.gov/publications/detail/sp/800-57-part-1/rev-4/final)