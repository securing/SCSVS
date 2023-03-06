# I2: Token

## Control Objective

If a project integrates with external Token smart contracts, it is necessary to approach them with limited trust and check that they do not introduce unexpected behavior into our system.

Ensure that a verified contract satisfies the following high-level requirements:
* Contract follows a tested and stable Token standard,
* The properties of the Token that we enter into our system are known and properly handled.
* Vulnerabilities identified in various Token implementations have been taken into account during implementation.

Category “I2” lists requirements related to the Token smart contract as one of the components with which the project integrates.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **I2.1** | Verify that there are no vulnerabilities associated with Token integrations. |
| **I2.2** | Verify if the external Token implementation is compliant with the standard implementation. |
| **I2.3** | Verify if the rules on which a new external Token can be added to the system have been defined (no restrictions, any tokens added by Governance, etc.).  |
| **I2.4** | Verify that the allowlist approach is used when only selected tokens are introduced to the system. |
| **I2.5** | Verify if the external Token implementation is non-standard (e.g. it is deflationary, or contains a fee), it has been taken into consideration. |
| **I2.6** | Verify that if the external Token implementation includes external calls, it has been taken into consideration (e.g., protection against reentrancy). |
| **I2.7** | Verify that the external Token magnitude (decimals) are known and that all operations are executed with the correct magnitude. |
| **I2.8** | Verify that the external Token supply is specified and corresponds to the documentation. |
| **I2.9** | Verify that the external Tokens of any user cannot be locked or frozen by any entity (e.g., owner). |
| **I2.10** | Verify that the reentrancy attack has been considered when using the token contracts with callbacks (e.g. ERC-777, ERC-721, ERC-1155). |
| **I2.11** | Verify that transfer of external Tokens has been successful, comparing the balances before and after it. |
| **I2.12** | Verify that project contracts handles correctly both types of tokens, those that return false on an error and those that revert. |
| **I2.13** | Verify that the contract reverts on failed transfer. |
| **I2.14** | Verify that the protocol handles double-entry tokens (tracking user balances in a contract represented by two addresses) correctly or forbids them. |
| **I2.15** | Use OpenZeppelin's SafeERC20 for interacting with ERC20 tokens. |

## References

For more information, see also:

* [Token Interaction Checklist Consensys](https://consensys.net/diligence/blog/2020/11/token-interaction-checklist/)
* [Token Integration Checklist ToB](https://github.com/crytic/building-secure-contracts/blob/master/development-guidelines/token_integration.md)
* [The Dangers of Token Integration](https://www.youtube.com/watch?v=6GaCt_lM_ak)
* [Token Implementation Best Practice](https://consensys.github.io/smart-contract-best-practices/tokens/)
* [iToken Duplication Incident Report](https://bzx.network/blog/incident)
* [The Dangers of Surprising Code](https://samczsun.com/the-dangers-of-surprising-code/)
* [ERC20 standard peculiarities](https://github.com/d-xo/weird-erc20)
