# V10: Token

## Control Objective

Ensure that a verified contract satisfies the following high-level requirements:
* The implemented token follows the security standards.

Category “V10” lists requirements related to the token of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **10.1** | Verify that the token contract follows a tested and stable token standard. |
| **10.2** | Use the approve function from the ERC-20 standard to change allowed amount only to 0 or from 0.  |
| **10.3** | Verify that the contract does not allow to transfer tokens to zero address. |
| **10.4** | Verify that the re-entracy attack has been considered when using the token contracts with callbacks (e.g. ERC-777). |
| **10.5** | Verify that the transfer business logic is consistent, especially when re-sending tokens to the same address (msg.sender == destination). |
| **10.6** | Verify that there are no vulnerabilities associated with Token. | 


## References

For more information, see also:

* [Token Implementation Best Practice](https://consensys.github.io/smart-contract-best-practices/tokens/)
* [iToken Duplication Incident Report](https://bzx.network/blog/incident)
* [The Dangers of Token Integration](https://www.youtube.com/watch?v=6GaCt_lM_ak)
