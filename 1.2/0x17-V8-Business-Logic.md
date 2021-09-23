# V8: Business logic

## Control Objective

To build secure smart contracts, we need to consider security of their business logic. Some of the smart contracts are influenced by vulnerabilities by their design.
The components used should not be considered safe without verification. Business assumptions should meet with the principle of minimal trust, which is essential in building smart contracts.

Ensure that a verified contract satisfies the following high-level requirements:
* The business logic flow is sequential and in order.
* Business limits are specified and enforced.
* Cryptocurrency and token business logic flows have considered abuse cases and malicious actors.

Category “V8” lists requirements related to the business logic of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **8.1** | Verify that the contract logic implementation corresponds to the documentation. | 
| **8.2** | Verify that the business logic flows of smart contracts proceed in a sequential step order and it is not possible to skip any part of it or to do it in a different order than designed.  | 
| **8.3** | Verify that the contract has business limits and correctly enforces it. | 
| **8.4** | Verify that the business logic of contract does not rely on the values retrieved from untrusted contracts with multiple calls of the same function. | 
| **8.5** | Verify that the contract logic does not rely on the balance of contract (e.g. balance == 0). | 
| **8.6** | Verify that the sensitive operations of contract do not depend on the block data (i.e. block hash, timestamp). | 
| **8.7** | Verify that the contract uses mechanisms that mitigate transaction-ordering dependence (front-running) attacks (e.g. pre-commit scheme). | 
| **8.8** | Verify that the contract does not send funds automatically but it lets users withdraw funds on their own in separate transaction instead. | 
| **8.9** | Verify that the inherited contracts do not contain identical functions or the order of inheritance is carefully specified. | 
| **8.10** | Verify that the business logic does not compare the extcodehash return value with 0 to check whether another address is contract (the hash of empty data is returned in such case). | 
| **8.11** | Verify that there are no vulnerabilities associated with business logic. | 


## References

For more information, see also:

* [Timestamp Dependence](https://consensys.github.io/smart-contract-best-practices/recommendations/#timestamp-dependence)
* [DASP 10: Front-Running](https://www.dasp.co/#item-7)
* [Front-Running (AKA Transaction-Ordering Dependence)](https://consensys.github.io/smart-contract-best-practices/known_attacks/)
* [Solidity Recommendations](https://consensys.github.io/smart-contract-best-practices/recommendations/)
* [SWC-125 Incorrect Inheritance Order](https://smartcontractsecurity.github.io/SWC-registry/docs/SWC-125)
* [EIP 1052: EXTCODEHASH Opcode](https://eips.ethereum.org/EIPS/eip-1052)
