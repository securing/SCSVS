# C1: Token

## Control Objective

If a project contains a Token smart contract, it is necessary to follow the standard and create a secure contract based on it. Learn from past mistakes that have been identified and have solutions ready.

Ensure that a verified contract satisfies the following high-level requirements:
* Contract follows a tested and stable Token standard,
* Vulnerabilities identified in various Token implementations have been taken into account during implementation.

Category “C1” lists requirements related to the Token smart contract as one of the project components.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **C1.1** | Verify that there are no vulnerabilities associated with Token component. |
| **C1.2** | Verify that token contract follows tested and stable Token standard. |
| **C1.3** | Verify that the security considerations of the standard used are known and handled by the team.  |
| **C1.4** | Verify that the total token supply matches the documentation. |
| **C1.5** | Verify that the number of minted and burned tokens does not disturb the operation of the system specified in the documentation. |
| **C1.6** | Verify that if the token contains a fee, its maximum value is predetermined and matches the documentation. |
| **C1.7** | Verify that the transfer business logic is consistent, especially when re-sending tokens to the same address (msg.sender == destination). |
| **C1.8** | Verify that if the implemented functions include external calls, they are handled correctly and do not introduce unsafe external calls to the system. |
| **C1.9** | Verify that the *approve()* function from the ERC-20 standard change the allowed amount only to 0 or from 0. |

## References

For more information, see also:

* [Token Implementation Best Practice](https://consensys.github.io/smart-contract-best-practices/tokens/)
* [iToken Duplication Incident Report](https://bzx.network/blog/incident)
* [The Dangers of Token Integration](https://www.youtube.com/watch?v=6GaCt_lM_ak)