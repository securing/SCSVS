# V10: Token

## Control Objective

Category “V10” lists requirements related to the token of the smart contracts.

## Security Verification Requirements

| # | Description | Since |
| --- | --- | --- |
| **10.1** | Verify that token contract follows tested and stable token standard. | 1.0 |
| **10.2** | Use the approve function of the ERC-20 standard to change allowed amount only to 0 or from 0  | 1.0 |
| **10.3** | Verify that contract does not allow to transfer tokens to zero address. | 1.0 |


## References

For more information, see also:

* [OWASP Threat Modeling Cheat Sheet](https://www.owasp.org/index.php/Threat_Modeling_Cheat_Sheet)
