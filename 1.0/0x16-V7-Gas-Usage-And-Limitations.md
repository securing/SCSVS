# V7: Gas usage & limitations

## Control Objective

Ensure that a verified contract satisfies the following high level requirements:
* TODO

Category “V7” lists requirements related to gas and smart contract limitations.

## Security Verification Requirements

| # | Description | Since |
| --- | --- | --- |
| **7.1** | Verify that the usage of gas in an smart contracts is be anticipated, defined and have clear limitations that can not be exceeded. Both, code structure and malicious input should not cause gas exhaustion. | 1.0 |
| **7.2** | Verify that two types of the addresses are considered when using *send* function. Sending Ether to contract address costs more that sending Ether to personal address. | 1.0 |
| **7.3** | Verify that the contract does not iterate over unbound loops. | 1.0 |
| **7.4** | Verify that the contract does not check whether the address is a contract using *extcodesize* opcode. | 1.0 |
| **7.5** | Verify that contract does not generate pseudorandom numbers trivially basing on the information from blockchain (e.g. seeding with the block number). | 1.0 |
| **7.6** | Verify that contract does not assume fixed-point precision and use a multiplier or store both the numerator and denominator. | 1.0 |
| **7.7** | Verify that, if signed transactions are used for relaying, the signatures are created in the same way for every possible flow to prevent replay attacks. | 1.0 |
| **7.8** | Verify that there exists a mechanism that protects contract from a replay attacks in case of hard-fork. | 1.0 |
| **7.9** | Verify that all library functions that should be upgradeable are not internal. | 1.0 |
| **7.10** | Verify that the *external* keyword is used for functions that can be called externally only to save gas. | 1.0 |

## References

For more information, see also:

* TODO