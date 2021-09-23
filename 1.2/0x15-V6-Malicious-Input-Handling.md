# V6: Malicious input handling

## Control Objective

Values obtained as parameters by smart contracts should be validated.

Ensure that a verified contract satisfies the following high-level requirements:
* The function parameters being passed are handled in a safe and predictable manner.

Category “V6” lists requirements related to the malicious input to the functions of smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **6.1** | Verify that if the input (function parameters) is validated, the positive validation approach (allowlisting) is used where possible. |
| **6.2** | Verify that the length of the address being passed is determined and validated by smart contract. |
| **6.3** | Verify that there are no vulnerabilities associated with malicious input handling. |

## References

For more information, see also:

* [Security Considerations - Sending and Receiving Ether](https://solidity.readthedocs.io/en/v0.5.10/security-considerations.html#sending-and-receiving-ether)
* [OpenZeppelin: SafeMath](https://github.com/OpenZeppelin/openzeppelin-solidity/blob/master/contracts/math/SafeMath.sol)
