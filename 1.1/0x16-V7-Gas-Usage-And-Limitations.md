# V7: Gas usage & limitations

## Control Objective

The efficiency of gas consumption should be taken into account not only in terms of optimization, but also in terms of safety to avoid possible exhaustion. Smart contracts by nature have different limitations that, if they are not taken into account, can cause different vulnerabilities.

Ensure that a verified contract satisfies the following high-level requirements:
* The use of gas is optimized and unnecessary losses are prevented,
* The implementation is in line with the smart contracts' limitations.

Category “V7” lists requirements related to gas and smart contract limitations.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **7.1** | Verify that the usage of gas in the smart contract is anticipated, defined and has clear limitations that cannot be exceeded. Both, code structure and malicious input should not cause gas exhaustion. | 
| **7.2** | Verify that two types of the addresses are considered when using the send function. Sending Ether to the contract address costs more than sending Ether to the personal address. | 
| **7.3** | Verify that the contract does not iterate over unbound loops. | 
| **7.4** | Verify that the contract does not check whether the address is a contract using *extcodesize* opcode. | 
| **7.5** | Verify that the contract does not generate pseudorandom numbers trivially basing on the information from blockchain (e.g. seeding with the block number). | 
| **7.6** | Verify that the contract does not assume fixed-point precision but uses a multiplier or store both the numerator and denominator instead. | 
| **7.7** | Verify that, if signed transactions are used for relaying, the signatures are created in the same way for every possible flow to prevent replay attacks. | 
| **7.8** | Verify that there exists a mechanism that protects the contract from a replay attack in case of a hard-fork. | 
| **7.9** | Verify that all library functions that should be upgradeable are not internal. | 
| **7.10** | Verify that the *external* keyword is used for functions that can be called externally only to save gas. | 
| **7.11** | Verify that there is no hard-coded amount of gas assigned to the function call (the gas prices may vary in the future). | 
| **7.12** | Verify that there are no vulnerabilities associated with gas usage & limitations. | 

## References

For more information, see also:

* [DASP 10: Bad Randomness](https://www.dasp.co/#item-6)
* [Gas Limit and Loops](https://solidity.readthedocs.io/en/v0.5.10/security-considerations.html#gas-limit-and-loops)
* [Insufficient gas griefing](https://consensys.github.io/smart-contract-best-practices/known_attacks/#insufficient-gas-griefing)
* [SWC-121 Missing Protection against Signature Replay Attacks](https://smartcontractsecurity.github.io/SWC-registry/docs/SWC-121)
* [EIP 150: Gas cost changes for IO-heavy operations](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-150.md)
* [EIP 1344: ChainID opcode](https://eips.ethereum.org/EIPS/eip-1344)
