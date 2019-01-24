# V2: Limitations

## Control Objective

[Description]

Category “V2” lists requirements related to the limitations of the smart contracts.

## Security Verification Requirements

| # | Description | L1 | L2 | L3 | Since |
| --- | --- | --- | --- | -- | -- |
| **1.1** | Do not generate pseudorandom numbers basing on the information from blockchain (eg. seeding with the block numer). |  | ✓ | ✓ | 1.0 |
| **1.2** | The usage of gas in an smart contracts should be anticipated, defined and have clear limitations that can not be exceeded. Both, code structure and malicious input should not cause gas exhaustion. |  | ✓ | ✓ | 1.0 |
| **1.3** | Make sure that you take into account two types of the addresses when using send(). Sending ether to contract address costs more that sending ether to personal address.  |  | ✓ | ✓ | 1.0 |
| **1.4** | Flow of contract should not be depend on the block data (ie. block hash, timestamp). |  | ✓ | ✓ | 1.0 |
| **1.5** | Make sure you employ mechanisms against a replay attacks in case of hard-fork. |  | ✓ | ✓ | 1.0 |


## References

For more information, see also:

* [OWASP Threat Modeling Cheat Sheet](https://www.owasp.org/index.php/Threat_Modeling_Cheat_Sheet)
* [OWASP Attack Surface Analysis Cheat Sheet](https://www.owasp.org/index.php/Attack_Surface_Analysis_Cheat_Sheet)
* [OWASP Threat modeling](https://www.owasp.org/index.php/Application_Threat_Modeling)
* [OWASP Secure SDLC Cheat Sheet](https://www.owasp.org/index.php/Secure_SDLC_Cheat_Sheet)
* [Microsoft SDL](https://www.microsoft.com/en-us/sdl/)
* [NIST SP 800-57](https://csrc.nist.gov/publications/detail/sp/800-57-part-1/rev-4/final)