# G12: Test coverage

## Control Objective

Ensure that a verified contract satisfies the following high-level requirements:
* The specification has been formally tested,
* The implementation has been tested statically and dynamically,
* The implementation has been tested using symbolic execution.

Category “G12” lists requirements related to the testing process of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **G12.1** | Verify that there are no recommendations regarding the needed improvement test coverage in the external company audit report.  |
| **G12.2** | Verify that abuser stories specified during threat modeling are covered by unit tests.  |  
| **G12.3** | Verify that considered sensitive functions of the verified contract are covered with tests in the development phase. |
| **G12.4** | Verify that the implementation of the verified contract has been checked for security vulnerabilities using static and dynamic analysis. |
| **G12.5** | Verify that the specification of the smart contract has been formally verified.  | 
| **G12.6** | Verify that the specification and the result of formal verification are included in the documentation.  | 
| **G12.7** | Verify that *solidity-coverage* indicates excellent code coverage. |

## References

For more information, see also:

* [Formal Verification](https://docs.soliditylang.org/en/latest/smtchecker.html#smtchecker-and-formal-verification)
* [Slither](https://github.com/crytic/slither)
* [Code coverage for Solidity testing](https://github.com/sc-forks/solidity-coverage)
* [MythX Plugin for Truffle](https://github.com/ConsenSys/truffle-security)
* [Securify](https://securify.chainsecurity.com/)
* [SmartCheck](https://tool.smartdec.net/)
* [Oyente](https://github.com/melonproject/oyente)
