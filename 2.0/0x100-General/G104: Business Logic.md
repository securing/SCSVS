# G104: Business logic

## Control Objective

To build secure smart contracts, we need to consider security of their business logic. Some of the smart contracts are influenced by vulnerabilities by their design.
The components used should not be considered safe without verification. Business assumptions should meet with the principle of minimal trust, which is essential in building smart contracts.

Ensure that a verified contract satisfies the following high-level requirements:
* The business logic flow is sequential and in order.
* Business limits are specified and enforced.
* Cryptocurrency and token business logic flows have considered abuse cases and malicious actors.

Category “G104” lists requirements related to the business logic of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **104.1** | Verify that there are no vulnerabilities associated with business logic. | 
| **104.2** | Verify that the contract logic and protocol parameters implementation corresponds to the documentation. | 
| **104.3** | Verify that the business logic flows of smart contract proceed in a sequential step order and it is not possible to skip any part of it or to do it in a different order than designed.  | 
| **104.4** | Verify that the contract has business limits and correctly enforces it. | 
| **104.5** | Verify that the business logic of contract does not rely on the values retrieved from untrusted contracts (especially when there are multiple calls to the same contract in one flow). | 
| **104.6** | Verify that the contract logic does not rely on the balance of contract (e.g., *balance == 0*). | 
| **104.7** | Verify that the sensitive operations of contract do not depend on the block data (e.g., *block hash*, *timestamp*). | 
| **104.8** | Verify that the contract uses mechanisms that mitigate transaction-ordering dependence (front-running) attacks (e.g. pre-commit scheme). | 
| **104.9** | Verify that the contract does not send funds automatically, but it lets users withdraw funds on their own in separate transaction instead. | 

## References

For more information, see also:

* [Timestamp Dependence](https://consensys.github.io/smart-contract-best-practices/recommendations/#timestamp-dependence)
* [DASP 10: Front-Running](https://www.dasp.co/#item-7)
* [Front-Running (AKA Transaction-Ordering Dependence)](https://consensys.github.io/smart-contract-best-practices/known_attacks/)
* [Solidity Recommendations](https://consensys.github.io/smart-contract-best-practices/recommendations/)
* [SWC-125 Incorrect Inheritance Order](https://smartcontractsecurity.github.io/SWC-registry/docs/SWC-125)
* [EIP 1052: EXTCODEHASH Opcode](https://eips.ethereum.org/EIPS/eip-1052)
