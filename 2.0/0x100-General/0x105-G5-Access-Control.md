# G5: Access control

## Control Objective

Access control is the process of granting or denying specific requests to obtain and use information and related information processing services.

Ensure that a verified contract satisfies the following high-level requirements:
* Users and other contracts are associated with a well-defined set of roles and privileges,
* Access is granted only to privileged users and contracts.

Category “G5” lists requirements related to the access control mechanisms of the smart contracts.

## Security Verification Requirements

| # | Description |
| --- | --- |
| **G5.1** | Verify that there are no vulnerabilities associated with access control. | 
| **G5.2** | Verify that the principle of the least privilege exists. Other contracts should only be able to access functions and data for which they possess specific authorization. | 
| **G5.3** | Verify that new contracts with access to the audited contract adhere to the principle of minimum rights by default. Contracts should have minimal or no permission until access to the new features is explicitly granted. | 
| **G5.4** | Verify that the creator of the contract complies with the rule of the least privilege and that their rights strictly follow the documentation. |
| **G5.5** | Verify that the contract enforces the access control rules specified in a trusted contract, especially if the dApp client-side access control is present and could be bypassed. | 
| **G5.6** | Verify that the calls to external contracts are allowed only if necessary. | 
| **G5.7** | Verify that the code of modifiers is clear and simple. The logic should not contain external calls to untrusted contracts. | 
| **G5.8** | Verify that all user and data attributes used by access controls are kept in a trusted contract and cannot be manipulated by other contracts unless specifically authorized. | 
| **G5.9** | Verify that the access controls fail securely, including when a revert occurs. | 
| **G5.10** | Verify that if the input (function parameters) is validated, the positive validation approach (allowlisting) is used where possible. | 
| **G5.11** | Verify that passing priviledged access to another address is two-step operation. |

## References

For more information, see also:

* [OWASP Cheat Sheet: Access Control](https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/Access_Control_Cheat_Sheet.md)
* [OpenZeppelin: Access Control]([https://github.com/OpenZeppelin/openzeppelin-solidity/blob/852e11c2dbb19a4000decacf1840f5e4c29c5543/docs/access-control.md#role-based-access-control](https://docs.openzeppelin.com/contracts/3.x/access-control))
