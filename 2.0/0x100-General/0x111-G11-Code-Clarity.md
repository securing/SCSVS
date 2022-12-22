# G11: Code clarity

## Control Objective

Ensure that a verified contract satisfies the following high-level requirements:
* The code is clear and easy to read,
* There are no unwanted or unused parts of the code,
* Variable names are in line with good practices,
* The functions being used are secure.

Category “G11” lists requirements related to the code clarity of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **G11.1** | Verify that there are no recommendations regarding needed improvement of code clarity in the external company audit report. | 
| **G11.2** | Verify that the logic is clear and modularized in multiple simple contracts and functions. | 
| **G11.3** | Verify that there is a description  in  the  form  of  1-2  short sentences of what the contract is for at the beginning of the contract. | 
| **G11.4** | Verify that if the system uses a ready-made implementation of the contract, it has been marked in the comment. If it contains changes from the original, those have been specified. |
| **G11.5** | Verify that the inheritance order is considered for contracts that use multiple inheritance and shadow functions.  | 
| **G11.6** | Verify that the contract uses existing and tested code (e.g. token contract or mechanisms like *ownable*) instead of implementing its own. | 
| **G11.7** | Verify that the same rules for variable naming are followed throughout all the contracts (e.g. use the same variable name for the same object). | 
| **G11.8** | Verify that variables with similar names are not used. | 
| **G11.9** | Verify that all storage variables are initialized. | 
| **G11.10** | Verify that the functions which specify a return type return the value. | 
| **G11.11** | Verify that all functions and variables are used. Unused ones should be removed. | 
| **G11.12** | Verify that the *require* function is used instead of the *revert* function in *if* statement. | 
| **G11.13** | Verify that the *assert* function is used to test for internal errors and the *require* function is used to ensure a valid condition on the input from users and external contracts. | 
| **G11.14** | Verify that assembly code is used only if necessary. | 

## References

For more information, see also:

* [Solidity Style Guide v0.8.17](https://docs.soliditylang.org/en/v0.8.17/style-guide.html)
* [Solidity: Security Considerations & Recommendations](https://solidity.readthedocs.io/en/v0.5.10/security-considerations.html#recommendations)
