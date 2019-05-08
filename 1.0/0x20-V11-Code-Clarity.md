# V11: Code clarity

## Control Objective

Ensure that a verified contract satisfies the following high level requirements:
* The code is clear and easy to read.
* There are no unwanted or unused parts of the code.
* Variable names are in line with good practices.
* Used functions are secure.

Category “V11” lists requirements related to the code clarity of the smart contracts.

## Security Verification Requirements

| # | Description | Since |
| --- | --- | --- |
| **11.1** | Verify that the logic is clear and modularized in multiple simple contracts and functions. | 1.0 |
| **11.2** | Verify that the inheritance order is considered for contracts that use multiple inheritance and shadow functions.  | 1.0 |
| **11.3** | Verify that the contract uses existing and tested code (e.g. token contract or mechanisms like *ownable*) instead of implementing its own. | 1.0 |
| **11.4** | Verify that the same rules for variable naming are followed throughout all the contracts (e.g. use the same variable name for the same object). | 1.0 |
| **11.5** | Verify that variables with similar names are not used. | 1.0 |
| **11.6** | Verify that all variables are defined as storage or memory variable. | 1.0 |
| **11.7** | Verify that all storage variables are initialised. | 1.0 |
| **11.8** | Verify that constructor keyword is used for solidity version greater than 0.4.24. For older versions of solidity make sure the constructor name is the same as contract's name. | 1.0 |
| **11.9** | Veryfy that functions which specify a return type return the value. | 1.0 |
| **11.10** | Verify that all functions are used and remove unused ones. | 1.0 |
| **11.11** | Verify that *require* function is used instead of *revert*  function in *if* statement. | 1.0 |
| **11.12** | Verify that *assert* function is used to test for internal errors and *require* function is used to ensure valid condition on input from users and external contracts. | 1.0 |
| **11.13** | Verify that assembly code is used only if necessary. | 1.0 |



## References

For more information, see also:

* [OWASP Threat Modeling Cheat Sheet](https://www.owasp.org/index.php/Threat_Modeling_Cheat_Sheet)
