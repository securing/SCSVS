# V10: Token

## Control Objective

Ensure that a verified contract satisfies the following high level requirements:
* Implemented token follows security standards.

Category “V10” lists requirements related to the token of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **10.1** | Verify that token contract follows tested and stable token standard. |
| **10.2** | Use the approved function of the ERC-20 standard to change allowed amount only to 0 or from 0.  |
| **10.3** | Verify that contract does not allow to transfer tokens to zero address. |


## References

For more information, see also:

* [Token Implementation Best Practice](https://consensys.github.io/smart-contract-best-practices/tokens/)
