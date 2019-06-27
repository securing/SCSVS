# V7: Gas usage & limitations

## Control Objective

The efficiency of gas consumption should be taken into account not only in terms of optimization, but also in terms of safety to avoid possible exhaustion. Smart contracts by nature have different limitations that, if they are not taken into account, can cause different vulnerabilities.

Ensure that a verified contract satisfies the following high level requirements:
* The use of gas is optimized and unnecessary losses are prevented,
* The implementation is in line with the smart contracts limitations.

Category “V7” lists requirements related to gas and smart contract limitations.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **7.1** | Verify that the usage of gas in a smart contracts is anticipated, defined and have clear limitations that can not be exceeded. Both, code structure and malicious input should not cause gas exhaustion. | 
| **7.2** | Verify that two types of the addresses are considered when using the send function. Sending Ether to contract address costs more that sending Ether to personal address. | 
| **7.3** | Verify that the contract does not iterate over unbound loops. | 
| **7.4** | Verify that the contract does not check whether the address is a contract using *extcodesize* opcode. | 
| **7.5** | Verify that contract does not generate pseudorandom numbers trivially basing on the information from blockchain (e.g. seeding with the block number). | 
| **7.6** | Verify that contract does not assume fixed-point precision and use a multiplier or store both the numerator and denominator. | 
| **7.7** | Verify that, if signed transactions are used for relaying, the signatures are created in the same way for every possible flow to prevent replay attacks. | 
| **7.8** | Verify that there exists a mechanism that protects contract from a replay attacks in case of hard-fork. | 
| **7.9** | Verify that all library functions that should be upgradeable are not internal. | 
| **7.10** | Verify that the *external* keyword is used for functions that can be called externally only to save gas. | 

## References

For more information, see also:

* TODO