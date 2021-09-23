# V11: Code clarity

## Control Objective

Ensure that a verified contract satisfies the following high-level requirements:
* The code is clear and easy to read,
* There are no unwanted or unused parts of the code,
* Variable names are in line with good practices,
* The functions being used are secure.

Category “V11” lists requirements related to the code clarity of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **11.1** | Verify that the logic is clear and modularized in multiple simple contracts and functions. | 
| **11.2** | Verify that the inheritance order is considered for contracts that use multiple inheritance and shadow functions.  | 
| **11.3** | Verify that the contract uses existing and tested code (e.g. token contract or mechanisms like *ownable*) instead of implementing its own. | 
| **11.4** | Verify that the same rules for variable naming are followed throughout all the contracts (e.g. use the same variable name for the same object). | 
| **11.5** | Verify that variables with similar names are not used. | 
| **11.6** | Verify that all variables are defined as storage or memory variable. | 
| **11.7** | Verify that all storage variables are initialised. | 
| **11.8** | Verify that the constructor keyword is used for Solidity version greater than 0.4.24. For older versions of Solidity make sure the constructor name is the same as contract's name. | 
| **11.9** | Verify that the functions which specify a return type return the value. | 
| **11.10** | Verify that all functions are used. Unused ones should be removed. | 
| **11.11** | Verify that the *require* function is used instead of the *revert* function in *if* statement. | 
| **11.12** | Verify that the *assert* function is used to test for internal errors and the *require* function is used to ensure a valid condition on the input from users and external contracts. | 
| **11.13** | Verify that assembly code is used only if necessary. | 
| **11.14** | Verify that there is a description  in  the  form  of  1-2  short sentences of what the contract is for at the beginning of the contract. | 
| **11.15** | Verify that if the system uses a ready-made implementation of the contract, it has been marked in the comment. If it contains changes from the original, those have been specified. |



## References

For more information, see also:

* [Solidity: Security Considerations & Recommendations](https://solidity.readthedocs.io/en/v0.5.10/security-considerations.html#recommendations)
