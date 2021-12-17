# I302: Token

## Control Objective

If a project integrates with external Token smart contracts, it is necessary to approach them with limited trust and check that they do not introduce unexpected behavior into our system.

Ensure that a verified contract satisfies the following high-level requirements:
* Contract follows a tested and stable Token standard,
* The properties of the Token that we enter into our system are known and properly handled.
* Vulnerabilities identified in various Token implementations have been taken into account during implementation.

Category “I302” lists requirements related to the Token smart contract as one of the project components.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **302.1** | Verify that there are no vulnerabilities associated with Token integrations. |
| **302.2** | Verify if the external Token implementation is compliant with the standard implementation. |
| **302.3** | Verify if the rules on which a new external Token can be added to the system have been defined (no restrictions, any tokens added by Governance etc.).  |
| **302.4** | Verify that the allowlist approach is used when only selected tokens are introduced to the system. |
| **302.5** | Verify if the external Token implementation is non-standard (e.g. it  is deflationary, contains a fee), it has been taken into consideration. |
| **302.6** | Verify that if the external Token implementation includes external calls, it has been taken into consideration (e.g., protection against reentrancy). |
| **302.7** | Verify that the external Token magnitude (decimals) are known, and all operations are executed with the correct magnitude. |
| **302.8** | Verify that the external Token supply is specified and corresponds to the documentation. |
| **302.9** | Verify that the external Tokens of any user cannot be locked or frozen by any entity (e.g., owner). |
| **302.10** | Verify that the reentrancy attack has been considered when using the token contracts with callbacks (e.g. ERC-777). |
| **302.11** | Verify that transfer of external Tokens has been successful, comparing the balances before and after it. |
| **302.12** | Verify that projects contracts uses *safeTransfer* function which handles correctly both types of tokens, those that return false on error and those that revert. |
| **302.13** | Verify that the contract reverts on failed transfer. |

## References

For more information, see also:

* [The Dangers of Token Integration](https://www.youtube.com/watch?v=6GaCt_lM_ak)
* [Token Implementation Best Practice](https://consensys.github.io/smart-contract-best-practices/tokens/)
* [iToken Duplication Incident Report](https://bzx.network/blog/incident)