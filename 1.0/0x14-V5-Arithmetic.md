# V5: Arithmetic

## Control Objective

Ensure that a verified contract satisfies the following high level requirements:
* All mathematical operations and extreme variable values are handled in a safe and predictable manner.

Category “V5” lists requirements related to the arithmetic operations of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **5.1** | Verify that the values and math operations are resistant to integer overflows. Use SafeMath library for arithmetic operations. | 
| **5.2** | Verify that the extreme values (e.g. maximum and minimum values of the variable type) are considered and does change the logic flow of the contract. | 
| **5.3** | Verify that non-strict inequality is used for balance equality. | 

## References

For more information, see also:

* [DASP 10: Artithmetic Issues](https://www.dasp.co/#item-3)
* [OpenZeppelin: SafeMath](https://github.com/OpenZeppelin/openzeppelin-solidity/blob/master/contracts/math/SafeMath.sol)
* [SWC-101 Integer Overflow and Underflow](https://smartcontractsecurity.github.io/SWC-registry/docs/SWC-101)