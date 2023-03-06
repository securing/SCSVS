# G7: Arithmetic

## Control Objective

Ensure that a verified contract satisfies the following high-level requirements:
* All mathematical operations and extreme variable values are handled safely and predictably.

Category “G7” lists requirements related to the arithmetic operations of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **G7.1** | Verify that there are no vulnerabilities associated with arithmetic. | 
| **G7.2** | Verify that the values and math operations are resistant to integer overflows. Use *SafeMath* library for arithmetic operations before solidity 0.8.\*. | 
| **G7.3** | Verify that the unchecked code snippets from Solidity 0.8.\* do not introduce integer under/overflows. | 
| **G7.4** | Verify that the extreme values (e.g. maximum and minimum values of the variable type) are considered and do change the logic flow of the contract. | 
| **G7.5** | Verify that non-strict inequality is used for balance equality. | 
| **G7.6** | Verify that there is a correct order of magnitude in the calculations. | 
| **G7.7** | Verify that in calculations, multiplication is performed before division for accuracy. | 
| **G7.8** | Verify that contract does not assume fixed-point precision and use a multiplier or store both the numerator and denominator. | 
| **G7.9** | Verify that rounding uses secure granularity (e.g. seconds instead of days). |
| **G7.10** | Verify that rounding in extreme conditions (e.g. very often) does not cause amplified losses (e.g. lack of interests accrued). Use RayWad library for such calculations. |

## References

For more information, see also:

* [DASP 10: Arithmetic Issues](https://www.dasp.co/#item-3)
* [OpenZeppelin: SafeMath](https://github.com/OpenZeppelin/openzeppelin-solidity/blob/master/contracts/math/SafeMath.sol)
* [SWC-101 Integer Overflow and Underflow](https://smartcontractsecurity.github.io/SWC-registry/docs/SWC-101)
* [Significant Rounding Errors For Interest Calculation](https://github.com/OpenCoreCH/smart-contract-audits/blob/main/reports/c4/rigor.md#high-significant-rounding-errors-for-interest-calculation)
