# V8: Business logic

## Control Objective

To build secure smart contracs, we need to consider security of their business logic. Some of the smart contracts are influenced by vulnerrabilities by their design.
The components used should not be considered safe without verification. Business assumptions should meet with the principle of minimal trust, which is essential in building smart contracts.

Ensure that a verified contract satisfies the following high level requirements:
* The business logic flow is sequential and in order.
* Business limits are specified and enforced.
* Cryptocurrency and token business logic flows have considered abuse cases and malicious actors.

Category “V8” lists requirements related to the business logic of the smart contracts.

## Security Verification Requirements

| # | Description | Since |
| --- | --- | --- |
| **8.1** | Verify that contract logic implementation corresponds to the documentation. | 1.0 |
| **8.2** | Verify that business logic flows of smart contracts proceed in sequential step order and it is not possible to skip any part of it or do it in a different order than designed.  | 1.0 |
| **8.3** | Verify the contract has business limits and correctly enforces it. | 1.0 |
| **8.4** | Verify that the business logic of contract does not rely on the values retrieved from untrusted contracts with multiple calls of the same function. | 1.0 |
| **8.5** | Verify that you do not rely the contract logic on the balance of contract (e.g. balance == 0). | 1.0 |
| **8.6** | Verify that the sensitive operations of contract does not depend on the block data (ie. block hash, timestamp). | 1.0 |
| **8.7** | Verify that contract uses mechanisms that mitigate transaction-ordering dependence (front-running) attacks (e.g. pre-commit scheme). | 1.0 |
| **8.8** | Verify that contract does not send funds automatically, but lets users withdraw funds on their own in separate transaction. | 1.0 |
| **8.9** | Verify that inherited contracts does not contain identical functions or the order of inheritance is carefully specified. | 1.0 |


## References

For more information, see also:

* [Solidity Recommendations](https://consensys.github.io/smart-contract-best-practices/recommendations/)
* [SWC-125 Incorrect Inheritance Order](https://smartcontractsecurity.github.io/SWC-registry/docs/SWC-125)