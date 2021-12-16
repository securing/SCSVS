# G112: Test coverage

## Control Objective

Ensure that a verified contract satisfies the following high-level requirements:
* The specification has been formally tested,
* The implementation has been tested statically and dynamically,
* The implementation has been tested using symbolic execution.

Category “G112” lists requirements related to the testing process of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **112.1** | Verify that there are no recommendations regarding the needed improvement test coverage in the external company audit report.  |
| **112.2** | Verify that abuser stories specified during threat modeling are covered by unit tests.  |  
| **112.3** | Verify that considered as sensitive functions of verified contract are covered with tests in the development phase. |
| **112.4** | Verify that the implementation of verified contract has been checked for security vulnerabilities using static and dynamic analysis. |
| **112.5** | Verify that the specification of smart contract has been formally verified.  | 
| **112.6** | Verify that the specification and the result of formal verification is included in the documentation.  | 

## References

For more information, see also:

* [Formal Verification](https://solidity.readthedocs.io/en/v0.5.10/security-considerations.html#formal-verification)
* [Code coverage for Solidity testing](https://github.com/sc-forks/solidity-coverage)
* [Remix IDE](https://remix.ethereum.org/)
* [MythX Plugin for Truffle](https://github.com/ConsenSys/truffle-security)
* [Securify](https://securify.chainsecurity.com/)
* [SmartCheck](https://tool.smartdec.net/)
* [Oyente](https://github.com/melonproject/oyente)
* [Security Tools](https://consensys.github.io/smart-contract-best-practices/security_tools/)