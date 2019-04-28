# V2: Access control

## Control Objective

Access control is the process of granting or denying specific requests to obtain and use information and related information processing services. Ensure that a verified contract satisfies the following high level requirements:
* Users and other contracts are associated with a well-defined set of roles and privileges.
* Access is granted to privileged users and contracts.

Category “V2” lists requirements related to the access control mechanisms of the smart contracts.

## Security Verification Requirements

| # | Description | Since |
| --- | --- | --- |
| **2.1** | Verify that the principle of least privilege exists - other contracts should only be able to access functions and data for which they possess specific authorization. | 1.0 |
| **2.2** | Verify that the principle of deny by default exists whereby new contracts that are allowed to access the audited contract start with minimal or no permissions and do not receive access to new features until access is explicitly granted. | 1.0 |
| **2.3** | Verify that the creator of the contract complies the rule of least privilege and his rights strictly follows the documentation. The ability to upgrade the libraries is a good practice. | 1.0 |
| **2.4** | Verify that the contract enforces access control rules specified in a trusted contract, especially if dApp client-side access control is present and could be bypassed. | 1.0 |
| **2.5** | Verify that there is a centralized mechanism for protecting access to each type of protected resource. | 1.0 |
| **2.6** | Verify that the calls to external contracts are allowed only if neccessary. | 1.0 |
| **2.7** | Verify that visibility of all functions is specified. | 1.0 |
| **2.8** | Verify that the initialization function are marked internal and cannot be executed twice. | 1.0 |
| **2.9** | Verify that the code of modifiers is clear and simple. The logic should not contain external calls to untrusted contracts. | 1.0 |
| **2.10** | Verify that contract relies on the data provided by right sender and contract does not rely on *tx.origin* value. | 1.0 |
| **2.11** | Verify that all user and data attributes used by access controls are kept in trusted contract and cannot be manipulated by other contracts unless specifically authorized. | 1.0 |
| **2.12** | Verify that access controls fail securely including when an revert occurs. | 1.0 |

## References

For more information, see also:

* [OWASP Cheat Sheet: Access Control](https://github.com/OWASP/CheatSheetSeries/blob/master/cheatsheets/Access_Control_Cheat_Sheet.md)