# C3: Oracle

## Control Objective

If a project builds an Oracle smart contract, it is necessary to follow the standard and create a secure contract based on it. Learn from past mistakes that have been identified and have solutions ready.

Ensure that a verified contract satisfies the following high-level requirements:
* Contract follows a tested and stable Oracle standard,
* Manipulating the oracle's results is unprofitable and easy to detect,
* Vulnerabilities identified in various Oracle implementations have been taken into account during implementation.

Category “C3” lists requirements related to the Oracle smart contract as one of the project components.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **C3.1** | Verify that there are no vulnerabilities associated with the Oracle component. |
| **C3.2** | Verify that the manipulation of the returned data by Oracle is unprofitable for the attacker. |
| **C3.3** | Verify that there are alerts set and monitored for large and sudden changes in the price feed. |
| **C3.4** | Verify if there is a way to mark the data as incorrect. |
| **C3.5** | Verify that the supply with incorrect data is penalized. |
| **C3.6** | Verify that the value (e.g., price for an asset) returned by oracle cannot be influenced in a single block. |

## References

For more information, see also:

* [ORACLES](https://ethereum.org/en/developers/docs/oracles/)
* [The Dangers of Price Oracles in Smart Contracts](https://www.youtube.com/watch?v=YGO7nzpXCeA)
* [So you want to use a price oracle](https://samczsun.com/so-you-want-to-use-a-price-oracle/)
