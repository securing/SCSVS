# C5: Liquidity Pool

## Control Objective

If a project contains a Liquidity Pool smart contract, it is necessary to follow the standard and create a secure contract based on it. Learn from past mistakes that have been identified and have solutions ready.

Ensure that a verified contract satisfies the following high-level requirements:
* Contract follows a tested and stable Liquidity Pool standard,

Category “C5” lists requirements related to the Liquidity Pool smart contract as one of the project components.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **C5.1** | Verify that there are no vulnerabilities associated with Vault component. |
| **C5.2** | Verify that there is a minimal liquidity locked (e.g. 1000) on first deposit to liquidity pool. |

## References
For more information, see also:
* [Frontrunning first LP deposit](https://github.com/code-423n4/2022-04-jpegd-findings/issues/12)
* [Curve read-only reentrancy](https://chainsecurity.com/curve-lp-oracle-manipulation-post-mortem/)

