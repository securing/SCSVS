# V1: Business Logic Requirements

## Control Objective

To build secure smart contracs, we need to consider security of their business logic. Some of the smart contracts are influenced by vulnerrabilities by their design.

The components used should not be considered safe without verification. Business assumptions should meet with the principle of minimal trust, which is essential in building smart contracts.

Category “V1” lists requirements related to the business logic of the smart contracts.

## Security Verification Requirements

| # | Description | L1 | L2 | L3 | Since |
| --- | --- | --- | --- | -- | -- |
| **1.1** | Verify the code of hardcoded addresses. |  | ✓ | ✓ | 1.0 |
| **1.2** | Make sure you block recursive calls (reentrance) unless it is a must. |  | ✓ | ✓ | 1.0 |
| **1.3** | Make sure you check the result of calling functions (eg. send, transfer) from another contracts. |  | ✓ | ✓ | 1.0 |
| **1.4** | Verify that functions which specify a return type, return the value.  |  | ✓ | ✓ | 1.0 |
| **1.5** | Do not assume as catch-all function is safe. |  |  | ✓ | 1.0 |
| **1.6** | Do not use delegate calls in catch-all method. |  | ✓ | ✓ | 1.0 |
| **1.7** | Make sure that the creator of the contract, do not have too much power in the contract. |  | ✓ | ✓ | 1.0 |
| **1.8** | Make sure you rely on the data provided by right sender. Do not rely on tx.origin value. |  | ✓ | ✓ | 1.0 |
| **1.9** | Make sure you do not rely business logic on the values retrieved from other contracts with muptiple calls of the same function. | | ✓ | ✓ | 1.0 |
| **1.10** | Verify the contract will only process business logic flows in sequential step order, with all steps being processed in realistic human time, and not process out of order, skipped steps, process steps from another user, or too quickly submitted transactions. | | ✓ | ✓ | 1.0 |
| **1.11** | Verify the contract has business limits and correctly enforces it. | ✓ | ✓ | ✓ | 1.0 |

## References

For more information, see also:

* [OWASP Threat Modeling Cheat Sheet](https://www.owasp.org/index.php/Threat_Modeling_Cheat_Sheet)
* [OWASP Attack Surface Analysis Cheat Sheet](https://www.owasp.org/index.php/Attack_Surface_Analysis_Cheat_Sheet)
* [OWASP Threat modeling](https://www.owasp.org/index.php/Application_Threat_Modeling)
* [OWASP Secure SDLC Cheat Sheet](https://www.owasp.org/index.php/Secure_SDLC_Cheat_Sheet)
* [Microsoft SDL](https://www.microsoft.com/en-us/sdl/)
* [NIST SP 800-57](https://csrc.nist.gov/publications/detail/sp/800-57-part-1/rev-4/final)